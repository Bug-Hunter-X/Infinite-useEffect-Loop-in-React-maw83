# Infinite useEffect Loop in React

This repository demonstrates a common React bug: an infinite useEffect loop.  The useEffect hook is designed to perform side effects, but without a dependency array, it re-runs after every render, potentially leading to performance issues and unexpected behavior. This example showcases the problem and provides a solution.

## Bug

The `bug.js` file contains a component with a `useEffect` hook that lacks a dependency array. This causes the effect to run infinitely, logging a message to the console after every render triggered by the increment button. This is inefficient and demonstrates a common mistake when working with `useEffect`.

## Solution

The `bugSolution.js` file demonstrates the corrected version.  By adding the `count` variable to the dependency array, the effect only runs when the `count` value changes, preventing the infinite loop.