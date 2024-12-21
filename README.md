# React 19 useEffect Dependency Array Issue

This repository demonstrates a common issue encountered in React 19 when using `useEffect` hooks within `StrictMode`. The problem arises from an improperly managed dependency array, leading to unintended re-renders and potentially infinite loops.  The `bug.js` file shows the problematic code, while `bugSolution.js` provides the corrected version.

## Problem

In the initial `bug.js` implementation, the `useEffect` hook lacks the `count` variable in its dependency array. This causes the effect to run on every render, even if the count value hasn't changed, triggering an infinite render loop and console spam.  This is particularly noticeable when using `StrictMode`.

## Solution

The `bugSolution.js` file corrects this by including `count` in the dependency array. This ensures the effect only runs when the `count` value actually updates.