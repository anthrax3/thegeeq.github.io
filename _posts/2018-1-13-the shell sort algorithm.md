---
layout: post
title: The Shell Sort Algorithm
tags: [algorithm]
categories:
- blog
---
[Shell Sort](#) can be thought of as a more efficient variation of insertion
sort as it achieves this mainly by comparing items of varying distances apart
resulting in a run time complexity of O(n log <sup>2</sup> n). It is fairly 
straight forward but may seem somewhat confusing at first as it differs 
from other sorting algorithms in the way it selects items to
compare. 

Figure below shows shell sort being ran on an array of integers :-


![shellsort](http://blog.thegeeq.gq/images/shell-sort.png)

---
### THE ALGORITHM

{% highlight java %}

algorithm ShellSort(list)
  Pre: list 6 = ∅
  increment ← list.Count / 2
  Post: list has been sorted into values of ascending order
  while increment 6 = 0
   current ← increment
     while current < list.Count
       hold ← list[current]
       i ← current − increment
        while i ≥ 0 and hold < list[i]
          list[i + increment] ← list[i]
          i− = increment
        end while
       list[i + increment] ← hold
       current ← current + 1
     end while
     increment / = 2
   end while
   return list
end ShellSort

{% endhighlight %}

---

To see this in action click [Algonimate Shell Sort](http://algonimator.thegeeq.gq/#path=sorting/shell/basic).

And Yeah, That's all !!!

---
