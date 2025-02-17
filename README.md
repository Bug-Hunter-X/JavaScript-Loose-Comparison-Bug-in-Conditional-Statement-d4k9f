# JavaScript Loose Comparison Bug

This repository demonstrates a common JavaScript bug related to loose comparison (==) within a conditional statement.

## Bug Description
The function `foo` uses loose comparison (==) to check if two arguments are equal.  This can lead to unexpected results due to JavaScript's type coercion. For example, `0 == false` evaluates to `true`, even though they are of different types.  This might lead to incorrect logic in the function.

## Bug Reproduction
The `bug.js` file contains the buggy code.  You can reproduce the issue by running the following tests:

```javascript
console.log(foo(0, false)); // Unexpectedly returns true
console.log(foo(1, true));  // Unexpectedly returns true
console.log(foo('1', 1));  // Unexpectedly returns true
```

## Solution
The `bugSolution.js` file provides a corrected version of the function, using strict equality (===) to avoid type coercion issues.

## How to use
1. Clone the repository
2. Navigate to the directory in the command line.
3. Run `node bug.js` to observe the incorrect behavior.
4. Run `node bugSolution.js` to see the corrected behavior using strict equality.

This example highlights the importance of using strict equality (===) in JavaScript to ensure type safety and prevent unexpected behavior.