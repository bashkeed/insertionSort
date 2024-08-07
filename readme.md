# Insertion Sort Implementation in JavaScript

This repository contains a simple implementation of the Insertion Sort algorithm in JavaScript. The `insertionSort` function sorts an array of numbers in ascending order.

## Description

Insertion Sort is a simple sorting algorithm that builds the final sorted array one item at a time. It is much less efficient on large lists than more advanced algorithms such as quicksort, heapsort, or merge sort.

The algorithm iterates through the array, and for each element, it compares it with the elements before it and inserts it in the correct position by shifting the other elements.

## Implementation

The `insertionSort` function is implemented as follows:

```javascript
function insertionSort(arr) {
    for (let i = 1; i < arr.length; i++) {
        let currentValue = arr[i];
        let j;
        for (j = i - 1; j >= 0 && arr[j] > currentValue; j--) {
            arr[j + 1] = arr[j];
        }
        arr[j + 1] = currentValue;
        console.log(arr);
    }
    return arr;
}
```

## Usage

To use the insertionSort function, simply call it with an array of numbers as an argument. The function will print the array after each insertion step and return the sorted array.

### Example
```javascript
const sortedArray = insertionSort([23, 1, 10, 5, 2]);
console.log('Sorted Array:', sortedArray);
```

Output:

```less
[ 1, 23, 10, 5, 2 ]
[ 1, 10, 23, 5, 2 ]
[ 1, 5, 10, 23, 2 ]
[ 1, 2, 5, 10, 23 ]
Sorted Array: [ 1, 2, 5, 10, 23 ]
```

## How it Works

The function starts with the second element in the array (index 1).
1. It stores the current value and iterates through the sorted portion of the array (elements before the current element).
2. It shifts elements to the right until it finds the correct position for the current value.
3. It inserts the current value in the correct position.
4. It prints the array after each insertion step to show the progress of the sorting.
5. Finally, it returns the sorted array.

## Notes
* This implementation prints the array after each step to help visualize the sorting process.
* Insertion Sort has a time complexity of O(n^2) in the worst case, where n is the number of elements in the array. It is efficient for small data sets or nearly sorted arrays.
