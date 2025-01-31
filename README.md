# React useEffect: Forgetting to clear setInterval

This example demonstrates a common mistake in React's `useEffect` hook: forgetting to clear an interval using `clearInterval`. This can lead to memory leaks and unexpected behavior.

## Bug

The `bug.js` file contains a component that uses `setInterval` to update a counter every second. However, it fails to clear the interval when the component unmounts or when the dependency array changes. This results in the interval continuing to run indefinitely, even after the component is no longer needed. This causes a memory leak.

## Solution

The `bugSolution.js` file provides the corrected code. It uses `clearInterval` inside a `return` statement within `useEffect` to ensure the interval is always cleared, preventing memory leaks and ensuring correct component behavior.