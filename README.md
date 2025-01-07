# React 19 useEffect Hook Missing Dependency

This repository demonstrates a common error in React 19 related to the `useEffect` hook.  Specifically, it showcases how a missing dependency in the dependency array can lead to an infinite render loop. 

## The Problem
The `useEffect` hook in the provided `bug.js` file lacks the `count` variable in its dependency array. This causes the effect to run after every render, leading to an infinite loop and potential performance issues. The console logs show continuous rendering.

## The Solution
The `bugSolution.js` file fixes this issue by correctly including `count` in the dependency array. Now the effect only runs when the value of `count` changes.

## How to Reproduce
1. Clone this repository
2. Run `npm install`
3. Run `npm start`
4. Observe the console log and the behavior of the component in both `bug.js` and `bugSolution.js`