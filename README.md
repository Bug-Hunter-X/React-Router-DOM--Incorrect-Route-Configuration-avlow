# React Router DOM: Incorrect Route Configuration

This repository demonstrates a common error in React Router DOM involving incorrect route configuration.  The problem arises from the placement of the catch-all route ('*').  Improper placement can cause other routes to be ignored.

## Bug Description
The catch-all route, intended to handle 404 errors, is placed before other routes. This prevents other routes from matching and always shows the 404 page.

## Solution
The catch-all route should always be placed last in the Routes component. This ensures that it only matches when no other route matches.

## How to Reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Navigate to `/about`.  You'll see the 404 page instead of the About page.

## Solution Implemented
The solution is provided in `bugSolution.js`. The catch-all route is moved to the end of the route list.