# Express.js Unhandled Error in Route Handler

This repository demonstrates a common error in Express.js route handlers: lack of proper error handling. The `bug.js` file shows a route that fails to handle cases where the user ID is invalid, resulting in a server crash.  The `bugSolution.js` file provides a corrected version with comprehensive error handling and more informative error responses.

**Problem:** The original code assumes that the `userId` will always be valid and available. If a user tries to access a non-existent or improperly formatted `userId`, the application crashes without providing any meaningful information to the user.

**Solution:** The solution includes error handling to check if the `userId` is valid and the user exists, returning descriptive HTTP error codes and messages (400 Bad Request or 404 Not Found) instead of crashing the server.