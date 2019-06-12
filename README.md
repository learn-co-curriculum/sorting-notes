# Sorting

## Objectives
Student will be able to
* Explain why sorting is something we care about in computer science
* Determine the Big O of various sorting algorithms
* Evaluate the trade-offs between various sorting algorithms
* Implement an O(n^2) sorting algorithm based off written instructions
* Implement the "merge part" of a merge sort
* Have a starting point to explore things deeper independently

## Past Videos
* [manhattan 100917](https://www.youtube.com/watch?v=gybLbTQvMxI&feature=youtu.be)

## Prerequisites
It makes a lot more sense to do this after students have received at least some introductory content on Big O

## Notes
This lecture relies heavily on the notes in this repo [https://github.com/alexgriff/intro-to-sorting](https://github.com/alexgriff/intro-to-sorting).

There are definitely lots of ways to improve the delivery of this content, but this is a decent-ish starting point.

### Step 1: Why do we care?
Use the `randomArray.js` file and the `binarysearch.js` file (which also contains an implementation of a `linearSearch`) to review the concepts of a linear vs binary search.

Linear: doesn't matter if the array is sorted or unsorted. O(n). Look at every element.

Binary: If we know info about our data, we know that it has this property of being sorted, we can use that info to help us. Think of finding a word in a dictionary. You don't open to the first word and then look at the second, third, fourth etc. You open up to the middle and make decisions of the word you want is before or after. Each time throwing out an entire half of the dictionary. The size of the problem gets cut in half with each look up. Also, the input (n) _has to fully double in size_ to make our computer do 1 more piece of work. Slow growing. O(log n).

This is why sorting is so important. Even if the sorting algorithm is expensive or takes some amount of time, if you knew you had to repeatedly find elements in a collection it would be worth it to do the sorting up front to reap the benefits later.

### Step 2: The O(n^2) sorts
Cover the following using the notes, visualizations and code linked to in the [sorting repo](https://github.com/alexgriff/intro-to-sorting)
* Selection Sort
* Insertion Sort
* Briefly mention Bubble Sort, not implemented here, show Obama video if you want.

If you supply students with the `swap` function for `selectionSort`, having them implement the rest is a good breakout exercise.

### Step 3: Transition
The insight into why O(n^2) is so expensive is that in Quadratic Time

if we double the size of input (n), the algo runs 4x slower (n * n)
```
5 * 5 = 25
10 * 10 = 100
```

The flip side of this is that:

if we half the size of the input (n / 2), the algo runs in one-fourth (1/4)x time

Can we use this to our advantage?

If we had two sorted halves, can we produce full sorted result?

### Step 4: O( n * log n ) Sorts
Cover the following using the notes, visualizations, and code linked to in the [sorting repo](https://github.com/alexgriff/intro-to-sorting)
* Merge Sort
* Quick Sort

Quicksort is probs the hardest to implement. Go through slowly. Merge sort is very much within reach of students to implement. They should be able to conceptually follow the recursive part and implement the linear merge part.

Show Algorythmics dancing videos if you want.
