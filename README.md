# Inaccurate Dimensions using Dimensions.get('window') in React Native

This repository demonstrates a common issue in React Native where using `Dimensions.get('window')` to obtain screen dimensions can lead to inaccurate results, particularly after orientation changes.

The `bug.js` file contains the problematic code, while `bugSolution.js` presents a solution using the `onLayout` event or the `useDimensions` hook for more reliable dimension retrieval.

## Problem

`Dimensions.get('window')` retrieves the dimensions only once during the initial render.  When the screen orientation changes, the component doesn't automatically update its dimensions, leading to layout problems and incorrect rendering.

## Solution

The preferred approach involves using the `onLayout` event on the `View` component or leveraging a custom hook that uses the `Dimensions` API and `useEffect` to handle updates effectively.