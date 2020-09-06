---
layout: post
title:  "CS Fundamentals"
date:   2020-09-06 17:19:03 +1000
categories: learning cs
---

I had my first CS interview (albeit on a smaller scale) the other day and I think I let myself down. I probably should've spent more time studying CS fundamentals and less time studying networking or [RPL](https://andyluu.com/learning/cs/2020/08/30/understandingRPL.html). In hindsight it's definitely something that I should understand well before going into any CS interview. The key areas that I needed to work on further were: 

## 1. Sorting
- The different sorting algorithms had appeared in multiple different courses that I had done, but there were a few gaps in my knowledge:
    - **Quicksort**: 
    I'd watched a lecture about quicksort, but my recollection boiled down to "partition the array into smaller sub-arrays that get recursively sorted" (why is it even called quicksort? what if someone finds a quicker sorting algorithm one day? why not call it something more descriptive like pivotsort or partitionsort?). After watching a [few](https://www.youtube.com/watch?v=XE4VP_8Y0BU&t=1s) [YouTube](https://www.youtube.com/watch?v=Hoixgm4-P4M) [explanations](https://www.youtube.com/watch?v=x2LEyLvW0Lw) I wrote up an implementation in Python which hopefully solidifies quicksort in my mind.
    - **Why use one sorting algorithm over another?**: At the very least the name is a good reminder that quicksort is on average faster than mergesort, but I didn't know why. **Short answer**: The constant factors of nlogn are smaller. **Long answer:** [probably not worth remembering.](https://cs.stackexchange.com/questions/3/why-is-quicksort-better-than-other-sorting-algorithms-in-practice). I remembered that insertion sort is better than mergesort / quicksort for small n, but forgot what situations bubble sort is useful in (when the array is mostly sorted already)

## 2. Time and Space Complexity
- There's some overlap with sorting here in the understanding of why one algorithm is better than another but that's easy to remember and something I got mostly right anyway. What I need to work on here is the fundamental skill of reading some code or considering different solutions to a problem and figuring out in your head what the time and space complexity is.

- I think it's something that I'm actually okay at, but during the interview I know I rarely felt 100% confident about it. To some extent I think doing heaps and heaps of Leetcode problems and evaluating the solutions will help here. A related skill that I've never really thought about and I think will be useful is the ability to look at a problem and come up with different solutions based on different requirements e.g. constant space.

## 3. Arrays, Linked Lists and Memory
- [CS50 Introduction to Computer Science](https://andyluu.com/jekyll/update/2020/05/31/learning-the-basics.html) had some great coverage of these topics in the context of C, but my time with that course was almost a year ago and definitely needed some revision. I had an okay time with remembering how fast they could get values, set values, add values etc. but I mixed them up pretty easily. It's definitely a better idea to remember how these operations actually work at a low level and then I can determine the time complexity on my own.

All in all, I'm really glad I experienced my first CS interview in a fairly low-pressure environment. Even though I think I performed pretty poorly it was a good indication of the gaps in my knowledge and interview preparation and I'm going to be in a much better spot whenever my next CS interview is!
