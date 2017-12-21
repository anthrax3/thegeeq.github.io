---
layout: post
title: The Chrome's Dino Game
tags: [hacks]
categories:
- blog
---

Few Days Back, I was doing an experiment at my friend's home. For some research, while I was browsing on
his computer, the internet connection was lost. At that time, I was browsing on chrome, and one of our
other friends challenged us to defeat him in the [Chrome's Dino Game](#). So, we decided that till the 
connection is restored, we will play the game. As I wasn't in habit of playing that game, I was unable 
to beat his highest score, but I said him, *"Wait, I'll hack the game"*. 

Then, in approx 10 minutes I hacked the game & *beated the shit out of him*.

If you're also interested in hacking the game, then follow the steps given below ---

---

### Let's Start Hacking (¬‿¬)

1. Load up the Chrome Browser.

2. If you aren't connected to the Internet, then just search anything in the *address bar*.

3. Make sure you are on the *No Internet Connection* page.

4. Press `Space` and the game will start.

5. If any of the above steps doesnt work, then just type `chrome://dino` in the *address bar*.

6. Press `ctrl+shift+j` from the keyboard to open up the Chrome Console & type the commands in that 
   console as specified below.

7. **The Hacking Phase -**

   `Runner.prototype` lists all the availaible commands.
    Before using the commands, store the original values in a variable. 
    And when you are finished playing the game, restore the values.
    For example - 
    *Storing Values:* `var a = Runnner.prototype.function`
    *Restoring Values:* `Runnner.prototype.function = a`

    Some of the usual commands for :-

    *Tweaking the Speed:*
  `   Runner.instance_.setSpeed(1000)`,or any other speed other than 1000 and press enter. 
    
    *Becoming Immortal:*
  `   Runner.prototype.gameOver=function (){console.log("thegeeq")}`

---

Congrats !!!! You just hacked the Chrome Dino Game !!!! Happy Hacking</>.

