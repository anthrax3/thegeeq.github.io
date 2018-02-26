---
layout: post
title: Cracking the RSA Encryption
tags: [hacking, hacks]
categories:
- blog
---

**RSA** *is an algorithm used by modern computers to encrypt and decrypt messages.* It is an asymmetric cryptographic algorithm.
*Asymmetric means that there are two different keys. This is also called public key cryptography, because one of them can be
given to everyone. The other key must be kept private.* It is based on the fact that finding the factors of an integer is hard
(the factoring problem).

**RSA stands for Ron Rivest, Adi Shamir and Leonard Adleman**, who first publicly described it in 1978. A user of RSA creates
and then publishes the product of two large prime numbers, along with an auxiliary value, as their public key. The prime
factors must be kept secret. Anyone can use the public key to encrypt a message, but with currently published methods, if
the public key is large enough, only someone with knowledge of the prime factors can feasibly decode the message.

It is very simple to multiply numbers together, especially with computers. But it can be very difficult to factor numbers.
For example, if I ask you to multiply together 34537 and 99991, it is a simple matter to punch those numbers into a
calculator and 3453389167. But the reverse problem is much harder.

Suppose I give you the number 1459160519. I'll even tell you that I got it by multiplying together two integers. Can you tell
me what they are? This is a very difficult problem. A computer can factor that number fairly quickly, but (although there are
some tricks) it basically does it by trying most of the possible combinations. For any size number, the computer has to check
something that is of the order of the size of the square-root of the number to be factored. In this case, that square-root is
roughly 38000.

Now it doesn't take a computer long to try out 38000 possibilities, but what if the number to be factored is not ten digits,
but rather 400 digits? The square-root of a number with 400 digits is a number with 200 digits. The lifetime of the universe
is approximately 10<sup>18</sup> seconds - an 18 digit number.

Assuming a computer could test one million factorizations per second, in the lifetime of the universe it could check
10<sup>24</sup> possibilities. But for a 400 digit product, there are 10<sup>200</sup> possibilities. 
This means the computer would have to run for 10<sup>176</sup> times the life of the universe to factor the large number.

It is, however, not too hard to check to see if a number is prime--in other words to check to see that it cannot be factored.
If it is not prime, it is difficult to factor, but if it is prime, it is not hard to show it is prime.

So RSA encryption works like this. I will find two huge prime numbers, 'p' and 'q' that have 100 or maybe 200 digits each.
I will keep those two numbers secret (they are my private key), and I will multiply them together to make a number 'N=p*q'.
That number 'N' is basically my public key. It is relatively easy for me to get 'N'; I just need to multiply my two numbers.
But if you know $N$, it is basically impossible for you to find 'p' and 'q'. To get them, you need to factor 'N', which
seems to be an incredibly difficult problem.

But exactly how is 'N' used to encode a message, and how are 'p' and 'q' used to decode it? Below is presented a complete
example, but I will use tiny prime numbers so it is easy to follow the arithmetic. In a real RSA encryption system, keep in
mind that the prime numbers are huge.

In the following example, suppose that person A wants to make a public key, and that person B wants to use that key to send A
a message. In this example, we will suppose that the message A sends to B is just a number. We assume that A and B have
agreed on a method to encode text as numbers. Here are the steps:

 1. Person A selects two prime numbers. We will use 'p=23' and 'q=41' for this example, but keep in mind that the real
    numbers person A should use should be much larger.

 2. Person A multiplies 'p' and 'q' together to get pq = (23)*(41) = 943. '943' is the public key, which he tells
    to person B (and to the rest of the world, if he wishes).

 3. Person A also chooses another number 'e' which must be relatively prime to '(p-1)(q-1)'. In this case,
   (p-1)(q-1) = (22)(40) = 880, so e=7 is fine. 'e' is also part of the public key, so B also is told the value
    of 'e'.

 4. Now B knows enough to encode a message to A. Suppose, for this example, that the message is the number M=35.

 5. B calculates the value of C = M<sup>e<sup> (mod N) => 35<sup>7</sup> (mod 943).

 6. 35<sup>7</sup> = 64339296875 and $64339296875 (mod 943) = 545. The number '545' is the encoding that B sends to A.

 7. Now A wants to decode 545. To do so, he needs to find a number 'd' such that ed = 1 [mod(p-1)(q-1)], or
    in this case, such that 7d = 1*(mod(880)). A solution is d=503, since 7*503 = 3521 = 4(880) + 1 = 1*[mod(880)]

 8. To find the decoding, A must calculate C<sup>d</sup> (mod N) = 545<sup>503</sup>(mod 943). This looks like it will be a      horribl
    calculation, and at first it seems like it is, but notice that 503 = 256 + 128 + 64 + 32 + 16 + 4 + 2 + 1
    (this is just the binary expansion of 503). So this means that :-

    545<sup>503</sup> = 545<sup>256+128+64+32+16+4+2+1</sup> = 545<sup>256</sup>*545<sup>128</sup>.....*545<sup>1</sup>

But since we only care about the result (mod 943), we can calculate all the partial results in that modulus, and by
repeated squaring of 545, we can get all the exponents that are powers of 2.

For example, 545<sup>2</sup> * (mod(943)) = 545*545 = 297025*(mod 943) = 923.
Then square again: 545<sup>4</sup> (mod 943) = (545<sup>2</sup>)<sup>2</sup> (mod 943) = 923*923 = 851929 (mod 943) = 400, and so on.

We obtain the following table:<br>
   545<sup>1</sup>*(mod 943) = 545<br>
   545<sup>2</sup>*(mod 943) = 923<br>
   545<sup>4</sup>*(mod 943) = 400<br>
   545<sup>8</sup>*(mod 943) = 633<br>
   545<sup>16</sup>*(mod 943) = 857<br>
   545<sup>32</sup>*(mod 943) = 795<br>
   545<sup>64</sup>*(mod 943) = 215<br>
   545<sup>128</sup>*(mod 943) = 18<br>
   545<sup>256</sup>*(mod 943) = 324<br>

So the result we want is:<br>

 545<sup>503</sup>*(mod 943) = 324*18*215*795*857*400*923*545*(mod 943) = 35

Using this tedious (but simple for a computer) calculation, A can decode B's message and obtain the
original message 'N = 35'.

---
