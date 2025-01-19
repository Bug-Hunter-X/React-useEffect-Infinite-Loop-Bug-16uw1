# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by an incorrect dependency array.

## Bug Description
The `useEffect` hook is used to perform side effects after a component renders. If the dependency array is missing a value that changes on every render, the effect will run repeatedly, creating an infinite loop.

## Bug Solution
The solution is to include all values from the component's scope that the effect depends on in the dependency array. In this case, the `count` variable needs to be included.