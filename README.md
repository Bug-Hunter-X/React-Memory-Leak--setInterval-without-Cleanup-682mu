# React Memory Leak: setInterval without Cleanup

This repository demonstrates a common error in React applications involving the use of `setInterval` within the `useEffect` hook without proper cleanup. This leads to memory leaks and unexpected behavior.

## Problem
The `setInterval` function, when used within `useEffect` without a cleanup function, continues to run even after the component unmounts. This results in memory leaks and can cause performance issues. The bug.js file illustrates this problematic code.

## Solution
The `bugSolution.js` file provides a corrected version of the code. It includes a cleanup function that uses `clearInterval` to stop the interval when the component unmounts, resolving the memory leak.