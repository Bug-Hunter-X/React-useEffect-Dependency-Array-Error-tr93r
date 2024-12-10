# React useEffect Dependency Array Bug

This repository demonstrates a common error in React's `useEffect` hook:  forgetting to include state variables in the dependency array.  This can lead to unexpected re-renders and performance issues.

## Bug Description

The `bug.js` file contains a component that uses `useEffect` to log the current count.  However, the `count` variable is missing from the dependency array. This means that the effect will run after every render, regardless of whether the count has actually changed.

## Solution

The `bugSolution.js` file shows the corrected code.  The `count` variable is now included in the dependency array, ensuring the effect only runs when the count changes.  This improves performance and avoids unnecessary re-renders.