# React Router Catch-All Route Bug

This repository demonstrates a common issue with React Router's catch-all route (`/*`).  The `/*` route is intended to handle any unmatched routes, however, in certain setups, it intercepts all routes and prevents other route matches from working properly.

## Problem

The provided `App.js` shows a simple React Router setup. Despite having routes defined for `/` and `/about`, the catch-all route (`/*`) always renders, displaying a 404 page.  This happens even when navigating to `/` or `/about`.

## Solution

The issue is solved in `AppSolution.js` by changing the order of routes. The catch-all route (`/*`) must come after all other more specific routes. This ensures that the more specific routes are evaluated first.