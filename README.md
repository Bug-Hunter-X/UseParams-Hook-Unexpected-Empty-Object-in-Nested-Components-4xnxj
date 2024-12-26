# useParams Hook Unexpected Empty Object in Nested Components

This repository demonstrates a common issue encountered when using the `useParams` hook in React Router v6.  The problem arises when attempting to access route parameters from components that are not direct children of the route defining those parameters.  The solution provides a correct approach to handle this scenario using techniques like prop drilling or context API.

## Problem
The provided `NestedParamsBug.jsx` demonstrates the issue.  `useParams` within the `Grandchild` component returns an empty object despite the parent route having defined parameters. This is because `useParams` only works correctly within the scope of the route's immediate children.