# React: Memory Leak in useEffect Hook with setInterval
This repository demonstrates a common mistake when using the `setInterval` function within a React `useEffect` hook.  Forgetting to clear the interval leads to a memory leak. This example showcases the problematic code and its corrected version.

## Problem
The initial `MyComponent` uses `setInterval` to update a counter every second. However, it fails to include a cleanup function to clear the interval when the component unmounts or updates. This results in the interval continuing to run indefinitely, leading to unnecessary memory consumption and potential performance issues. 

## Solution
The corrected version includes a cleanup function within the `useEffect` hook's return value.  This function uses `clearInterval` to stop the interval when the component is no longer needed. This prevents memory leaks and ensures efficient resource management. 
