# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers:  the lack of error handling when dealing with user input.  Specifically, this example shows a route that retrieves a user by ID, but fails to handle the case where the provided ID is not a valid number.

## Bug

The `bug.js` file contains the flawed route handler.  It attempts to parse the user ID as an integer using `parseInt()`, but doesn't check if the result is actually a number or handle the scenario where `parseInt()` returns `NaN`. This leads to an error if a non-numeric ID is provided.

## Solution

The `bugSolution.js` file demonstrates the corrected route handler.  It adds error handling to check if the parsed ID is a valid number and returns an appropriate HTTP error response if it's not.