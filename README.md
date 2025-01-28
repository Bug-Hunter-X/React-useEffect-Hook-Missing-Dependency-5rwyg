# React useEffect Hook Missing Dependency

This repository demonstrates a common error in React's `useEffect` hook: omitting dependencies from the dependency array.  This can lead to unexpected behavior, including stale closures and performance issues.

## The Bug

The `bug.js` file contains a component that uses `useEffect` to log the current `count` to the console.  However, the `count` variable is missing from the dependency array. This means the effect only runs once after the initial render, regardless of changes to `count`.

## The Solution

The `bugSolution.js` file demonstrates the correct usage of `useEffect`.  By including `count` in the dependency array, the effect will run whenever the `count` value changes, ensuring that the logged value is always up-to-date.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console logs and the behavior of the button.