---
layout: post
title: Bubble Sort
tags: [algorithm]
categories:
- blog
---
[Bubble Sort](#) is one of the *most simple forms of sorting* is that of 
comparing each item with every other item in some list, 
however as the description may imply this form of sorting is not 
particularly efficient O(n<sup>2</sup>). 

In it’s most simple form bubble sort can be implemented as two loops.
---

### General Algorithm

<code>
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
</code>
---
