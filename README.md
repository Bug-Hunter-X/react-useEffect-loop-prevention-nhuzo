# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook. The bug arises when the dependency array is omitted or incorrectly specified, leading to an infinite loop of re-renders.

## Bug Description

The `useEffect` hook in the provided `MyComponent` function lacks a dependency array. As a result, the effect runs after every render, causing the component to constantly re-render and trigger the effect again, resulting in an infinite loop.

## Solution

The solution is to specify a dependency array in the `useEffect` hook. This ensures that the effect only runs when the values in the dependency array change. In this case, adding `[count]` as a dependency prevents the effect from running on every render, effectively resolving the infinite loop.

## How to Reproduce

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.
5. Observe the console output and the continuous re-rendering in your browser's developer tools.