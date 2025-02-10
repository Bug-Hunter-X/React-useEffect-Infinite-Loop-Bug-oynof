# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving an infinite loop within the `useEffect` hook.  The bug arises from an improper dependency array causing the effect to run on every render, creating an infinite loop.

## Bug Description
The `MyComponent` uses `useState` and `useEffect` to display and increment a counter. The `useEffect` hook has an incorrect dependency array, leading to an infinite loop. The condition `if (count > 0)` doesn't prevent the effect from triggering with every `setCount` update, since `count` is included in the dependency array.

## Bug Solution
The solution involves fixing the dependency array or refactoring the logic to avoid triggering the `useEffect` repeatedly.