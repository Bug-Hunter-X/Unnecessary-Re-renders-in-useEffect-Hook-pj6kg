# Unnecessary Re-renders in React 19 useEffect Hook

This repository demonstrates a common issue in React 19 where a `useEffect` hook runs after every render due to a missing dependency array. This leads to unnecessary re-renders and potential performance problems.

## Bug
The `bug.js` file shows a simple counter component. The `useEffect` hook inside logs the current count to the console after every render. Because there's no dependency array, it runs on every state change, causing excessive console logging and unnecessary work.

## Solution
The `bugSolution.js` file demonstrates how to fix the issue. By adding `[count]` as the dependency array to the `useEffect` hook, it now only runs when the `count` state variable changes. This significantly improves performance by preventing unnecessary re-renders and log outputs. 