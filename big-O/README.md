# Big-0 Notation

What is Big O Notation?

```
"Big O notation is a mathematical notation that describes the limiting behavior of a function when the argument tends towards a particular value or infinity."
```

[Wikipedia’s definition of Big O notation](https://en.wikipedia.org/wiki/Big_O_notation).

**Big-O in layman terms** is generally a way of analyzing how efficient an algorithm is. We can model how much time a function will take given n inputs `(n in this case is the length of an array)`

Given an example of a polynomial function such as: 3x^2 + 5x + 19

Big-O only cares about the `Dominant term` in this case the O(n^2).The O absorbs all the the terms.

Looking at another example: x^3 + 2x^2 - x - 2 our `dominant term` is O(n^3) where O absorbs all the other terms.

In an algorithm we could know the time it takes by checking the n input. Eg O(n^3) will `n*n*n` to go through the inputs.

When we go through an algorithm once with a for loop that translates to O(n)
for example:

```
const solveArray = () => {
  const myArray = [];
  for (let i = 9; i > 0; i -= 2) {
    myArray.push(i);
  }
  return myArray;
};

solveArray();
```

`O(n^2) 'Big O Squared'`

_For every input,we would go through a loop inside of another loop_

`Example:`

```
var arr = [
  [1, 2],
  [3, 4],
  [5, 6],
];
const showLength = (arr) => {
  const myArray = [];
  for (var i = 0; i < arr.length; i++) {
    for (var j = 0; j < arr[i].length; j++) {
      myArray.push(arr[i][j]);
    }
  }
  return myArray;
};

showLength(arr);
```

`O(1) 'Constant time'`

A function in which no matter how long the array is it takes a the same amount of time to get done. It contains only an exit/return statement.

`Example:`

```
const checkSum = (num1, num2) => {
  return num1 + num2;
};

checkSum(2, 3);
```

# Formal Definition of Big-O Notation

f(x) is O(g(x)) if there exist constants also known as `(witnesses)` C and k such that

`| f(x) | ≤ C .|g(x)| for all x ≥ k`

The formal definition is useful when you need to perform a math proof.
