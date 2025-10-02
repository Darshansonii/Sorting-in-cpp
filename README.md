# Sorting-in-cpp

--------------------------------------------------
AIM
--------------------------------------------------
The aim of this project is to implement and study various sorting algorithms in C++ including:
1. Bubble Sort
2. Bucket Sort
3. Heap Sort
4. Insertion Sort
5. Merge Sort
6. Quick Sort
7. Selection Sort

This project helps in understanding how data can be arranged in ascending or descending order, the efficiency of different sorting algorithms, and their applications.


--------------------------------------------------
THEORY
--------------------------------------------------
Sorting is the process of arranging elements in a specific order, typically ascending or descending.  
Sorting improves the efficiency of other algorithms like searching and is widely used in databases, graphics, and real-time systems.

### COMMON SORTING ALGORITHMS

1. **Bubble Sort**
   - Repeatedly swaps adjacent elements if they are in the wrong order.
   - Time Complexity: O(n^2)
   - Advantage: Simple to implement.
   - Limitation: Inefficient for large datasets.

2. **Insertion Sort**
   - Builds the sorted array one element at a time by inserting each new element at the correct position.
   - Time Complexity: O(n^2)
   - Advantage: Efficient for small or nearly sorted arrays.
   - Limitation: Slow for large datasets.

3. **Selection Sort**
   - Repeatedly selects the minimum (or maximum) element from unsorted part and places it at the beginning.
   - Time Complexity: O(n^2)
   - Advantage: Simple, performs well for small arrays.
   - Limitation: Inefficient for large arrays.

4. **Merge Sort**
   - Divide-and-conquer algorithm that splits the array, sorts the halves recursively, and merges them.
   - Time Complexity: O(n log n)
   - Advantage: Efficient and stable, works for large datasets.
   - Limitation: Requires extra memory for merging.

5. **Quick Sort**
   - Divide-and-conquer algorithm that selects a pivot, partitions the array around it, and recursively sorts partitions.
   - Time Complexity: O(n log n) on average, O(n^2) worst case
   - Advantage: Fast and in-place.
   - Limitation: Performance depends on pivot choice.

6. **Heap Sort**
   - Converts array into a binary heap, repeatedly extracts the maximum and rebuilds the heap.
   - Time Complexity: O(n log n)
   - Advantage: In-place, no recursion required.
   - Limitation: Not stable.

7. **Bucket Sort**
   - Distributes elements into several “buckets”, sorts each bucket, then concatenates them.
   - Time Complexity: O(n + k) (depends on distribution)
   - Advantage: Very fast for uniformly distributed data.
   - Limitation: Works best for floating-point numbers in a known range.


--------------------------------------------------
ALGORITHMS
--------------------------------------------------
BUBBLE SORT (arr[0..n-1])
1. Repeat for i = 0 to n-2
2.    For j = 0 to n-i-2
3.        If arr[j] > arr[j+1], swap them
4. End loops

INSERTION SORT (arr[0..n-1])
1. For i = 1 to n-1
2.    key = arr[i]
3.    j = i - 1
4.    While j >= 0 and arr[j] > key
5.        arr[j+1] = arr[j]
6.        j = j - 1
7.    arr[j+1] = key

SELECTION SORT (arr[0..n-1])
1. For i = 0 to n-2
2.    min_index = i
3.    For j = i+1 to n-1
4.        If arr[j] < arr[min_index], min_index = j
5.    Swap arr[i] and arr[min_index]

MERGE SORT (arr[low..high])
1. If low < high
2.    mid = (low + high) / 2
3.    Recursively sort arr[low..mid] and arr[mid+1..high]
4.    Merge the two sorted halves

QUICK SORT (arr[low..high])
1. If low < high
2.    Partition arr[low..high] using pivot
3.    Recursively sort left and right partitions

HEAP SORT (arr[0..n-1])
1. Build a max heap from array
2. For i = n-1 down to 1
3.    Swap arr[0] and arr[i]
4.    Reduce heap size by 1
5.    Heapify root

BUCKET SORT (arr[0..n-1])
1. Create n buckets (empty lists)
2. Distribute elements into buckets based on range
3. Sort each bucket individually
4. Concatenate all buckets in order


--------------------------------------------------
FILES
--------------------------------------------------
- Bubble Sort.cpp
- Bucket Sort.cpp
- Heap Sort.cpp
- Insertion Sort.cpp
- Merge Sort.cpp
- Quick Sort.cpp
- Selection Sort.cpp

Each file contains the C++ implementation of the respective sorting algorithm.


--------------------------------------------------
CONCLUSIONS
--------------------------------------------------
- Simple algorithms like Bubble, Insertion, and Selection Sort are easy to implement but inefficient for large datasets.
- Efficient algorithms like Merge Sort, Quick Sort, Heap Sort, and Bucket Sort are suitable for large arrays.
- Merge Sort is stable and reliable but requires extra memory.
- Quick Sort is very fast in practice but worst-case performance can be O(n^2) if pivot choice is poor.
- Heap Sort is in-place and avoids recursion but is not stable.
- Bucket Sort is highly efficient for uniformly distributed data but not suitable for all ranges.
- Understanding different sorting algorithms allows choosing the right technique for the problem based on data size, distribution, and memory constraints.
