# React Native useEffect Cleanup Function Error: Accessing State After Unmount

This repository demonstrates a common error in React Native applications involving the `useEffect` hook and its cleanup function.  The error arises when the cleanup function attempts to access or modify component state or props after the component has unmounted.  This often happens when dealing with asynchronous operations like subscriptions or timers.

## Problem
The provided `useEffectCleanupError.js` file showcases a scenario where a subscription's unsubscribe function might throw an error if the component is unmounted before the unsubscribe call completes.

## Solution
The `useEffectCleanupSolution.js` file presents a solution that addresses this issue by checking if the component is still mounted before attempting to access or modify its state. This ensures that no errors are thrown when the component unmounts.

## How to Reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run the app using a React Native simulator or device.
4. Observe the error in `useEffectCleanupError.js` and the correct behaviour in `useEffectCleanupSolution.js`.

## Technologies Used
* React Native
* JavaScript