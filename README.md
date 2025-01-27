# React Router Dom v6 - Route path="*" not catching unmatched routes

This repository demonstrates an unexpected behavior in React Router Dom v6 concerning the catch-all route (`path="*"`).  The issue is that the catch-all route is not functioning as expected, failing to match any unmatched routes. 

## Issue Description

The application includes routes for '/' and '/about'.  A catch-all route is added with `path="*"` to handle any other routes, rendering a 'Not Found' component. However, when navigating to a non-existent route, the 'Not Found' component is not displayed, rather, nothing is displayed and the UI remains unchanged.

## How to Reproduce

1. Clone this repository.
2. Install dependencies: `npm install`
3. Run the application: `npm start`
4. Navigate to a non-existent route (e.g., `/some-route`).

Expected Result: The 'Not Found' component should be rendered.
Actual Result: Nothing is rendered; the UI remains unchanged.

## Solution

The solution involves carefully reviewing the route configuration and ensuring the catch-all route (`path="*"`) is placed after all other specific routes. This has now been fixed in the solution file and described below.