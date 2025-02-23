# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by incorrectly specifying the dependency array.  The `useEffect` hook runs after every render. If you forget to include variables used inside the effect in its dependency array, the effect will trigger repeatedly, causing an infinite render loop.

## Problem
The `bug.js` file shows an example of this issue. The `useEffect` hook logs the count to the console, but because the count is not included in the dependency array, the effect reruns continuously causing the console to log messages repeatedly. 

## Solution
The `bugSolution.js` file demonstrates the correct usage of the dependency array.  By adding `count` to the dependency array, `useEffect` only runs when `count` changes.

## How to reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the infinite loop in the console (in `bug.js`).
5. Then, observe the correct behaviour in `bugSolution.js`
