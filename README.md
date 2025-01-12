# Unexpected Loop Behavior with setTimeout

This repository demonstrates a common JavaScript closure issue related to the use of `setTimeout` within a loop. The example showcases how the value of the loop variable `i` is not captured correctly within the callback function of `setTimeout`, leading to unexpected output.

## The Bug
The `myFunction()` function uses a `for` loop and `setTimeout` to log the value of `i` after a 1-second delay.  However, due to the nature of closures and how JavaScript handles variables in loops, all callbacks will log the final value of `i` (10) rather than the value of `i` at the time each `setTimeout` was called.