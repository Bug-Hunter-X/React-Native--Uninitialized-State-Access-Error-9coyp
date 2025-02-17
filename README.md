# React Native: Uninitialized State Access Error

This repository demonstrates a common error in React Native applications: attempting to access a state variable before it has been properly initialized.

The `bug.js` file shows the erroneous code, which results in a `TypeError: Cannot read properties of undefined (reading '...attribute...')` when the component tries to access a state property before the asynchronous operation that updates the state has completed.

The `bugSolution.js` file provides a corrected implementation using optional chaining and a conditional rendering to prevent the error.

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run the app on a simulator or device.
4. Observe the error in the console (in `bug.js`) and the correct behavior in `bugSolution.js`.

## Solution

The solution involves using optional chaining (`?.`) to safely access the property and conditional rendering to avoid rendering the component until the state is ready.