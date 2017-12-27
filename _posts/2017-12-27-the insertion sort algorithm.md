---
layout: post
title: The Insertion Sort Algorithm
tags: [algorithm]
categories:
- blog
---
[Insertion Sort](#) is a somewhat interesting algorithm with an expensive runtime of
O(n<sup>2</sup>). It can be best thought of as a sorting scheme similar to that of sorting
a hand of playing cards, i.e. you take one card and then look at the rest with
the intent of building up an ordered set of cards in your hand.

*It is a simple sorting algorithm which sorts the array by shifting elements one by one.*
It has one of the simplest implementation and is efficient for smaller data sets, but very
inefficient for larger lists. It is adaptive, that means it reduces its total number of 
steps if given a partially sorted list, hence it increases its efficiency.
It is better than Selection Sort and Bubble Sort algorithms. Its space complexity is less.
Like Bubble Sort, Insertion Sort also requires a single additional memory space.


![bubblesort](http://blog.thegeeq.gq/images/insertion-sort.png)

---
### THE ALGORITHM

{% highlight java %}

algorithm Insertionsort(list)
  Pre: list 6 = ∅
  Post: list has been sorted into values of ascending order
  unsorted ← 1
  while unsorted < list.Count
    hold ← list[unsorted]
    i ← unsorted − 1
    while i ≥ 0 and hold < list[i]
      list[i + 1] ← list[i]
      i ← i − 1
    end while
    list[i + 1] ← hold
    unsorted ← unsorted + 1
  end while
  return list
end Insertionsort

{% endhighlight %}

---

To see this in action click [Algonimate Insertion Sort](http://algonimator.thegeeq.gq/#path=sorting/insertion/basic).

And Yeah, That's all !!!

---
