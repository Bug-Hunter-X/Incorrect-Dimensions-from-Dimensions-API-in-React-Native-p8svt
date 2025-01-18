# React Native Dimensions API Inaccuracy

This repository demonstrates a common issue in React Native development involving the `Dimensions` API.  When accessing screen dimensions before the layout has fully calculated, the `Dimensions` API may return incorrect values. This leads to UI elements being rendered with inaccurate sizes or positions.

## Bug Description
The provided `bug.js` file shows an example where the `Dimensions` API is used within a component before the layout is complete.  This results in the `View` component receiving incorrect width and height values, causing it to render improperly.

## Solution
The `bugSolution.js` file presents a solution using the `onLayout` prop, which ensures the dimensions are obtained only after the component has fully laid out. This ensures accurate dimensions are used for rendering.