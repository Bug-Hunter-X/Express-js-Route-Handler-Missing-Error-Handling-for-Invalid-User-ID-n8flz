# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  Specifically, the provided code lacks validation for the user ID parameter, potentially leading to unexpected behavior or crashes if a non-numeric ID is provided.

The `bug.js` file contains the erroneous code. The `bugSolution.js` provides a corrected version with proper error handling.

## Bug
The primary issue is the absence of input validation. The code attempts to parse the `userId` as an integer using `parseInt()` without verifying that the input is actually a number. This could result in exceptions if a non-numeric string is supplied.

## Solution
The solution involves adding input validation.  Before attempting to parse the `userId`, the code checks if it's a number. If not, an appropriate error response is returned, preventing the application from crashing or returning unexpected results.