# Uncommon HTML Bug: Silent Failure on Non-Existent Element

This repository demonstrates a subtle bug in HTML involving attempts to manipulate the `innerHTML` property of a non-existent element. The script doesn't throw an error; instead, it silently fails, which can be difficult to trace.

The `bug.html` file contains the buggy code. The `bugSolution.html` file provides the corrected version.  This highlights the importance of robust error handling and checking for the existence of elements before manipulation.

## Bug Description:
The script attempts to change the `innerHTML` of an element with the ID `nonExistentElement`. Because this element doesn't exist in the HTML structure, the operation fails silently.  This is unlike many other JavaScript operations that would throw a more explicit error.

## Solution:
Always check if an element exists before manipulating its properties. Using `getElementById` returns `null` if the element isn't found.  The solution demonstrates how to incorporate this check for robust error handling.