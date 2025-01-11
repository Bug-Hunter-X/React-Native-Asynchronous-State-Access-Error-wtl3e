# React Native Asynchronous State Access Error

This repository demonstrates a common error in React Native applications: attempting to access a state variable before it's been initialized due to asynchronous operations.  The error, `TypeError: Cannot read properties of null (reading 'name')`, occurs when accessing a property of a state variable that is still `null`.

## Problem

The `bug.js` file contains code that fetches data from an API asynchronously.  It then attempts to render a component that uses the fetched data before it has been fully loaded.  This results in the error.

## Solution

The `bugSolution.js` file demonstrates how to solve this by using optional chaining (?.) and nullish coalescing (??).  This ensures that the component renders correctly even if the data is still loading.