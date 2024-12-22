# React useEffect Runs After Every Render
This repository demonstrates a common issue with the React `useEffect` hook where it runs after every render instead of only when the dependencies change.  The example showcases an infinite loop of console logs and unnecessary re-renders, highlighting the importance of specifying dependencies correctly.

## Bug Description
The provided code uses `useEffect` without specifying any dependencies.  This means the effect runs after every render, even if the `count` state hasn't changed, leading to unexpected behavior and potentially performance issues.

## Solution
The solution involves correctly specifying dependencies in the `useEffect` array. By specifying `[count]`, the effect only runs when the `count` state changes. This eliminates the performance problem and ensures the expected behavior.