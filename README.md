# Infinite Rendering Bug in React

This repository demonstrates a common React bug: infinite rendering caused by a missing dependency array in the `useEffect` hook. The component continuously re-renders because the `useEffect` hook lacks the `count` variable in its dependency array, triggering an infinite loop.

## Bug Description
The `MyComponent` uses the `useState` hook to manage a counter and the `useEffect` hook to log the render count. The `useEffect` hook lacks a dependency array, so it runs after every render causing the infinite loop. 

## Solution
The solution involves adding `count` to the dependency array of the `useEffect` hook, ensuring it only runs when the `count` value changes.

## How to reproduce
1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install`.
4. Run `npm start`.
5. Observe the infinite rendering in the browser's console.
