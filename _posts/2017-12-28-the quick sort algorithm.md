---
layout: post
title: The Insertion Sort Algorithm
tags: [algorithm]
categories:
- blog
---
[Quick Sort](#) is one of the *most popular sorting algorithms* based on *divide et*
*impera strategy*, resulting in an O(n log n) complexity. The algorithm starts by
picking an item, called *pivot*, and *moving all smaller items before it, while all*
*greater elements after it*. This is the main quick sort operation, called *partition,
recursively repeated on lesser and greater sub lists until their size is one or zero
- in which case the list is implicitly sorted.

Choosing an appropriate pivot, as for example the median element is funda-
mental for avoiding the drastically reduced performance of O(n<sup>2</sup>).

**Quick Sort**, as the name suggests, *sorts any list very quickly*. It is not a stable 
search, but it is *very fast and requires very less additional space.*
As stated above, It is based on the rule of *Divide and Conquer(also called partition-exchange sort).*
This algorithm divides the list into following three main parts :

1. Elements less than the Pivot element
2. Pivot element(Central element)
3. Elements greater than the pivot element

In the list of elements, mentioned in below example, I have taken 25 as pivot.


![quicksort](http://blog.thegeeq.gq/images/quick-sort.png)

---
### THE ALGORITHM

{% highlight java %}

algorithm QuickSort(list)
  Pre: list 6 = ∅
  Post: list has been sorted into values of ascending order
  if list.Count = 1 // already sorted
    return list
  end if
  pivot ←MedianValue(list)
  for i ← 0 to list.Count−1
    if list[i] = pivot
      equal.Insert(list[i])
    end if
    if list[i] < pivot
      less.Insert(list[i])
    end if
    if list[i] > pivot
      greater.Insert(list[i])
    end if
  end for
  return Concatenate(QuickSort(less), equal, QuickSort(greater))
end Quicksort

{% endhighlight %}

---

To see this in action click [Algonimate Quick Sort](http://algonimator.thegeeq.gq/#path=sorting/quick/basic).

And Yeah, That's all !!!

---
