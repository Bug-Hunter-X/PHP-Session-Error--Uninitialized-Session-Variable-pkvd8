# PHP Session Bug: Accessing Session Variable Before Initialization

This repository demonstrates a common PHP error: attempting to access a session variable before the session has been started using `session_start()`.  The `bug.php` file contains the erroneous code, while `bugSolution.php` provides the corrected version.

The issue arises because PHP doesn't automatically initialize sessions.  Accessing `$_SESSION` variables before calling `session_start()` leads to undefined index errors or unpredictable behavior.

## How to Reproduce

1. Clone this repository.
2. Run `bug.php` (you'll likely get a warning or error).
3. Run `bugSolution.php` to see the corrected implementation.

## Lesson Learned

Always call `session_start()` at the very beginning of your PHP script *before* accessing any session variables. This ensures that the session is properly initialized and prevents unexpected errors.