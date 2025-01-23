# Express.js Route Handler Missing Error Handling for Invalid User IDs

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling when dealing with user inputs.

The `bug.js` file contains code that's vulnerable to errors because it doesn't check if `req.params.id` can be safely converted to an integer.  This can lead to unexpected crashes or incorrect responses.

The `bugSolution.js` file provides a corrected version that includes comprehensive error handling to address the issue.  It checks the validity of the input before attempting the conversion, gracefully handling non-numeric IDs and providing a more robust user experience.

## How to reproduce the bug

1. Clone the repository.
2. Run `npm install express` to install the necessary dependency.
3. Run `node bug.js`.
4. Send a request to `/users/abc` or `/users/123a`. The application will likely crash due to the error.

## How to fix the bug

The solution is to properly validate and handle non-numeric user IDs.  Refer to the `bugSolution.js` file for the corrected implementation.