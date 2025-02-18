# React setInterval Memory Leak

This repository demonstrates a common error in React components that use `setInterval` without proper cleanup. This can lead to memory leaks in your application.

## Bug Description

The `MyComponent` component uses `setInterval` to update a counter every second. However, it fails to provide a cleanup function within the `useEffect` hook. This means that the interval continues to run even after the component unmounts. As a result, the component continues to be rendered, and the component continues to be rendered, resulting in a memory leak.

## Solution

The solution involves using the cleanup function provided by the `useEffect` hook to clear the interval when the component unmounts.