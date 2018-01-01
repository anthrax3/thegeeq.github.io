---
layout: post
title: The Merge Sort Algorithm
tags: [algorithm]
categories:
- blog
---
[Merge Sort](#) is an algorithm that has a fairly efficient space time complexity -
O(n log n) and is fairly trivial to implement. The algorithm is based on *splitting
a list, into two similar sized lists (lef t, and right) and sorting each list and then
merging the sorted lists back together.*

*Note: the function MergeOrdered simply takes two ordered lists and makes
them one.*

**Merge Sort** follows the rule of *Divide and Conquer*. In merge sort the unsorted 
list is divided into N sublists, each having one element, because a list consisting
of one element is always sorted. Then, it repeatedly merges these sublists, 
to produce new sorted sublists, and in the end, only one sorted list is produced.

*Merge Sort is quite fast* and is also a *stable sort*, which means the
"equal" elements are ordered in the same order in the sorted list.


![mergesort](http://blog.thegeeq.gq/images/merge-sort.png)

---
### THE ALGORITHM

{% highlight java %}

algorithm MergeSort(list)
  Pre: list 6 = ∅
  Post: list has been sorted into values of ascending order
  if list.Count = 1 // already sorted
    return list
  end if
  m ← list.Count / 2
  left ← list(m)
  right ← list(list.Count − m)
  for i ← 0 to lef t.Count−1
    left[i] ← list[i]
  end for
  for i ← 0 to right.Count−1
    right[i] ← list[i]
  end for
  left ← MergeSort(lef t)
  right ← MergeSort(right)
  return MergeOrdered(lef t, right)
end MergeSort

{% endhighlight %}

---

To see this in action click [Algonimate Merge Sort](http://algonimator.thegeeq.gq/#path=sorting/merge/basic).

And Yeah, That's all !!!

---
