# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The `useEffect` hook, when not properly managed with its dependency array, can lead to infinite re-renders and application crashes. This example shows how a missing dependency in the `useEffect` hook's dependency array can cause an infinite loop, and provides a solution.

## Bug

The `bug.js` file contains a React component that uses the `useEffect` hook to log a message to the console after every render. However, the `count` variable is not included in the dependency array.  This causes the effect to run on every render, leading to an infinite loop and a continuously updating console.

## Solution

The `bugSolution.js` file demonstrates the correct way to use the `useEffect` hook.  By adding `count` to the dependency array, the effect only runs when the `count` variable changes, preventing the infinite loop.