# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by a missing or incorrect dependency array.  The `useEffect` hook, when used improperly, can lead to performance issues and unexpected behavior.

## Bug Description

The provided `MyComponent` uses `useEffect` to log the current count to the console. However, because the dependency array `[count]` is missing, the effect runs after every render. This creates an infinite loop as updating the `count` triggers another render, leading to another effect execution, and so on.  This causes the console to spam and can significantly impact application performance.

## Solution

The solution involves adding the `count` variable to the dependency array.  This ensures the effect only runs when the `count` value changes.