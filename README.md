# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook. The bug causes an infinite loop due to a missing dependency in the `useEffect` call. 

## Bug Description

A component uses `useEffect` to log the render count.  However, the `count` state variable is missing from the dependency array. This means the effect runs on every render, updating the count, triggering another render, and creating an infinite loop.

## How to Reproduce

1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Open your browser and observe the console log; the 'Component rendered' message will appear continuously.

## Solution

The solution involves adding `count` to the dependency array of the `useEffect` hook. This ensures that the effect only runs when the `count` variable changes.