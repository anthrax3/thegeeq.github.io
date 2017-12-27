---
layout: post
title: The Bubble Sort Algorithm
tags: [algorithm]
categories:
- blog
---
[Bubble Sort](#) is one of the *most simple forms of sorting* is that of 
comparing each item with every other item in some list, 
however as the description may imply this form of sorting is not 
particularly efficient O(n<sup>2</sup>). 

**Bubble Sort** compares all the element one by one and sort them based on their values.
It is called Bubble sort, because *with each iteration the largest element in the 
list bubbles up towards the last place, just like a water bubble rises up to the water surface.*

Sorting takes place by stepping through all the data items one-by-one in pairs and comparing adjacent data items and swapping each pair that is out of order. *It works by repeatedly swapping the adjacent elements if they are in wrong order.*

![bubblesort](../images/bubblesort.png)

In it’s most simple form bubble sort can be implemented as two loops.

---
### THE ALGORITHM

{% highlight java %}

algorithm BubbleSort(list)
  Pre: list 6 = ∅
  Post: list has been sorted into values of ascending order
  for i ← 0 to list.Count − 1
	for j ← 0 to list.Count − 1
	  if list[i] < list[j]
	   swap(list[i], list[j])
	  end if
	end for
  end for
  return list
end BubbleSort

{% endhighlight %}

---

To see this in action click [Algonimate Bubble Sort](http://algonimator.thegeeq.gq/#path=sorting/bubble/basic).

And Yeah, That's all !!!

---
