# React Component Memory Leak

This repository demonstrates a common mistake in React components that can lead to memory leaks: using `setInterval` within the `useEffect` hook without proper cleanup.

The `bug.js` file contains the problematic code. The `setInterval` function is called without being cleaned up, causing a memory leak. The counter continues to increment even after the component unmounts.

The `bugSolution.js` file provides a corrected version of the code.  The `setInterval` is properly cleaned up in the cleanup function of the `useEffect` hook. This resolves the memory leak.