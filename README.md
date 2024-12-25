# Unhandled Promise Rejection in Express.js

This repository demonstrates a common error in Express.js applications: the lack of proper error handling for asynchronous operations.  When an asynchronous function throws an error, without a `.catch` block to handle it, the error might be silently ignored, leading to unexpected behavior. 

The `bug.js` file showcases this issue.  The `someAsyncOperation` function simulates an asynchronous action that can potentially fail.  If it fails, the error is not caught and the application continues without notifying the user.

The `bugSolution.js` file demonstrates how to correct the issue by adding proper error handling using `.catch` blocks. This ensures that errors are caught and handled gracefully.

## How to Reproduce

1. Clone this repository.
2. Navigate to the directory in your terminal.
3. Run `node bug.js`.
4. Observe that there is no output when the `someAsyncOperation` fails.  
5. Run `node bugSolution.js` and notice how error handling provides better logging.