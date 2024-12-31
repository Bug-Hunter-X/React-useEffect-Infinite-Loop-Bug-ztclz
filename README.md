# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug: an infinite loop caused by incorrectly updating state within the `useEffect` dependency array.  The `useEffect` hook runs after every render, and if it modifies state, it causes a re-render, triggering the `useEffect` again, leading to an infinite loop.

## Bug
The `bug.js` file contains the buggy code. The `useEffect` hook attempts to increment the count on every render, creating the infinite loop.  This will crash your React application.

## Solution
The `bugSolution.js` file provides a corrected version. The key is to only update the state when a condition is met, breaking out of the infinite loop scenario.  For example, you might use `useEffect` to fetch data only when the component mounts.