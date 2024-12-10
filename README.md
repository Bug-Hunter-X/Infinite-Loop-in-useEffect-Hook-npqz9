# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React applications involving the `useEffect` hook, specifically how incorrect usage can lead to an infinite loop. The bug involves updating a state variable within the `useEffect`'s dependency array, which triggers a continuous re-render and subsequent execution of the `useEffect`. 

## Bug Description
The `bug.js` file contains a component that attempts to increment a counter using `useEffect`.  However, because the `setCount` function modifies the `count` state, which is included in the dependency array of `useEffect`, an infinite render loop is created.  This can freeze the browser or cause unexpected behavior. 

## Solution
The `bugSolution.js` file provides a corrected version where the dependency array is left empty (`[]`), causing the useEffect to run only once after the initial render.  Alternatively, one could use a different state variable for the condition.   This addresses the infinite loop and prevents unexpected behavior.