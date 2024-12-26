# Uncommon HTML Bug: Accessing textContent Before innerHTML

This repository demonstrates a subtle bug in HTML/JavaScript that can occur when attempting to access the `textContent` of a DOM element before its `innerHTML` has been set.  The code incorrectly accesses a div's text content before setting its innerHTML, leading to an unexpected empty string rather than the intended content.

## Bug Description
The primary issue lies in the order of operations. The JavaScript code attempts to read the `textContent` of a div element before the `innerHTML` property is assigned a value. Since the element is initially empty, `textContent` returns an empty string.

## How to Reproduce
1. Clone this repository.
2. Open `bug.html` in a web browser.
3. Observe the console output. You'll see an empty string followed by the expected content.

## Solution
The solution is straightforward: Ensure that `innerHTML` is set *before* attempting to access `textContent` to avoid undefined behavior or unexpected output. See the `bugSolution.html` for the corrected code. 