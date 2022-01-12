# Sort Algorithms

## selection sort

**Pseudocode**: 

* repeat until no unsorted elements remain: 
  * search the unsorted part of the data to find the smallest value
  * swap the smallest found value with the first element of the unsorted part


![selection sort](assets/selection.gif)

## bubble
**Pseudocode**: 

* Set swap counter to a non-zero number
* Repeat until counter is 0
  * Reset swap counter to 0
  * Look at each adjacent pair
    * If two adjacent elements are not in order, swap them and add one to the swap counter

![bubble sort](assets/bubble.gif)

## merge sort

In merge sort, the idea of the algorithm is to sort smaller arrays and then combine those arrays together (merge them) in sorted order. Merge sort leverages **recursion**.

**Pseudocode**: 
If n > l
   1. Find the middle point to divide the array into two halves
   2. Call merge sort for first half
   3. Call merge sort for second half
   4. Merge the two halves sorted in step 2 and 3

![merge sort](assets/merge.gif)

[link to gifs](http://www-scf.usc.edu/~zhan468/public/Notes/sorting.html)