# Uncontrolled Re-renders in React useEffect Hook

This example demonstrates a common mistake in using the React `useEffect` hook: omitting dependencies.  When dependencies are missing, the effect runs after every render, often leading to infinite loops and significant performance degradation.

## Problem

The `useEffect` hook in `bug.js` lacks an empty dependency array (`[]`). This causes the `console.log` statement to execute on every render, creating an uncontrolled re-render cycle.

## Solution

`bugSolution.js` shows the correct implementation. By providing an empty dependency array (`[]`), the effect runs only once after the initial mount.  Alternatively, including specific dependencies ensures the effect only runs when those dependencies change.