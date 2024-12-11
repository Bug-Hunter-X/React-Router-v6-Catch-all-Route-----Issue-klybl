# React Router v6 Catch-all Route Issue

This repository demonstrates a problem encountered when using the catch-all route ('*') in React Router v6.  The expected behavior is that the NotFound component should render when navigating to a non-existent route, but this is not occurring.

## Setup

1. Clone the repository.
2. Navigate to the project directory.
3. Run `npm install`.
4. Run `npm start`.

## Steps to Reproduce

1. Navigate to `/` - Home component renders correctly.
2. Navigate to `/about` - About component renders correctly.
3. Navigate to any invalid route (e.g., `/invalid`) - **The NotFound component does not render, and the browser shows a blank page.**

## Solution

The issue is resolved by ensuring that the catch-all route is the last route defined in the routes configuration.  This is corrected in `bugSolution.js`.