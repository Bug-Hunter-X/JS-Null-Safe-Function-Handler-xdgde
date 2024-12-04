# JavaScript Function with Null Value Handling Bug

This repository demonstrates a common, yet subtle, bug in JavaScript functions related to null value handling. The `foo` function attempts to handle null values but may produce unexpected results when dealing with non-numeric input.

## Bug Description

The `foo` function is designed to add two numbers. It includes a check for null values in its parameters.  However, it doesn't explicitly check if the inputs are numbers. If the inputs are not numbers, the addition will lead to unexpected results which might result in an error or incorrect output. 

## How to Reproduce

1. Clone this repository.
2. Open `bug.js`
3. Run the script using a JavaScript runtime (Node.js, for example).  Observe the output for different input values, including null, numbers and non-numeric values. You will see that while it correctly handles explicit nulls it will fail if you pass in something like a string.

## Solution

The solution involves adding explicit type checking of the parameters to ensure they are numbers before performing addition.