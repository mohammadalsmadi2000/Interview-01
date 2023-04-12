# Interview-01

# Sum of Each Row in a Matrix

## Problem Domain
Given a matrix of integers, write a function that calculates the sum of each row and returns an array of those sums.

## Visual
![sum-of-each-row-and-column](https://user-images.githubusercontent.com/60603704/231557905-12ca9313-8b78-4ffd-8317-61be1105f9d5.jpg)


## Algorithm
1. Create an empty array to store the row sums.
2. Loop through each row in the matrix.
3. Create a variable to store the sum of the current row, starting at 0.
4. Loop through each element in the current row.
5. Add the value of the current element to the row sum.
6. After all elements have been added to the row sum, add the row sum to the array of row sums.
7. Return the array of row sums.

## Big O
1. Time Complexity: O(n^2) where n is the number of rows in the matrix, because we must iterate through each element in the matrix to calculate the row sums.
2. Space Complexity: O(n) where n is the number of rows in the matrix, because we are storing an array of row sums.

## Pseudocode

```
function sumEachRow(matrix):
  // create an empty array to store row sums
  rowSums = []
  
  // loop through each row
  for row in matrix:
    // create a variable to store the sum of the current row
    rowSum = 0
    
    // loop through each element in the row
    for element in row:
      // add the element value to the row sum
      rowSum += element
    
    // add the row sum to the array of row sums
    rowSums.push(rowSum)
    
  // return the array of row sums
  return rowSums

```

## Code

```
function sumEachRow(matrix) {
  const rowSums = [];
  
  for (const row of matrix) {
    let rowSum = 0;
    for (const element of row) {
      rowSum += element;
    }
    rowSums.push(rowSum);
  }
  
  return rowSums;
}

```

## Test

```
const matrix1 = [  [1, 2, 3],
  [3, 5, 7],
  [1, 7, 10]
];
console.log(sumEachRow(matrix1)); // [6, 15, 18]

const matrix2 = [  [0, 1, 5],
  [-4, 7, 2],
  [-3, 12, 11]
];
console.log(sumEachRow(matrix2)); // [6, 5, 20]

const matrix3 = [  [1, 0, -1],
  [0, 1, 0],
  [-1, 0, 1]
];
console.log(sumEachRow(matrix3)); // [0, 1, 0]

```
