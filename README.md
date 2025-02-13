# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common issue encountered when using closures within `setTimeout` loops in JavaScript.

## Problem
The `bug.js` file contains a function `myFunc` that uses a `for` loop and `setTimeout` to log the value of `i` after a delay.  Intuitively, one might expect the output to be 0, 1, 2...9. However, due to the way closures work in JavaScript, this is not the case.

## Solution
The `bugSolution.js` file provides a solution using an immediately invoked function expression (IIFE) to create a new scope for each iteration of the loop.  This ensures that each `setTimeout` callback captures its own independent value of `i`. 

## How to Run

1. Clone this repository.
2. Open `bug.js` and `bugSolution.js` in your preferred JavaScript environment.
3. Run `myFunc()` in `bug.js` and observe the unexpected output.
4. Run `myFunc()` in `bugSolution.js` and observe the correct output.