# React useEffect Hook Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The issue arises when the dependency array is omitted or incorrectly specified, leading to an infinite re-render loop.

## Bug Description

The `useEffect` hook in the `bug.js` file runs after every render because it's missing a dependency array. This causes an infinite loop because updating the `count` state triggers a re-render, which then triggers the `useEffect` again. The console will show a continuous log of the current count.

## Solution

The `bugSolution.js` file provides the corrected code. By adding `[count]` as the dependency array to the `useEffect` hook, it ensures that the effect only runs when the `count` state changes.