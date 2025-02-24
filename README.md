# Uncommon HTML Bug: NodeList Attribute Access

This repository demonstrates a subtle error that can occur when working with NodeLists in JavaScript within an HTML context. The bug arises from attempting to access an attribute that does not exist on a NodeList object.

## Bug Description
The `querySelectorAll` method returns a NodeList, which is a collection of nodes.  However, unlike individual elements, NodeLists do not have arbitrary attributes.  Attempting to access a non-existent attribute will throw a `TypeError`.

## Reproduction
1. Open `bug.html` in a web browser.
2. Observe the error in the browser's developer console.

## Solution
The solution involves iterating over the NodeList and accessing properties of individual nodes instead of trying to access properties of the NodeList itself.

## Solution Code
The `bugSolution.html` file shows the corrected code.