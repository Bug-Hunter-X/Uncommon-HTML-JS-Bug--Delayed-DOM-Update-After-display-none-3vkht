# Uncommon HTML/JS Bug: Delayed DOM Update

This repository demonstrates an uncommon bug related to manipulating the `display` property of an HTML element using JavaScript.  The issue involves setting an element's display to `none`, then later attempting to modify its contents and display after a delay.  The changes are not immediately reflected in the DOM rendering.

## The Bug
The `bug.html` file contains the buggy code. The main issue lies in using `setTimeout()` to modify the element. While the JavaScript code successfully updates the element, it doesn't render those changes immediately. This is an uncommon behavior as normally modifying an element directly after setting its display to "none" and then "block" would have it immediately updated.

## The Solution
The `solution.html` file provides a solution illustrating proper techniques for handling DOM manipulation after altering display property using requestAnimationFrame().