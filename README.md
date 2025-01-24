# Uninitialized Property Access in C#

This repository demonstrates a common error in C#: attempting to access a class property before it has been initialized. This can lead to a `NullReferenceException` at runtime.

The `Bug.cs` file contains the problematic code. The `BugSolution.cs` file shows how to fix it.

## Problem

In C#, class properties are reference types.  If not explicitly initialized, they have a default value of `null`. Attempting to use a `null` reference (in this case, performing arithmetic on `MyProperty` before it's assigned a value) will throw a `NullReferenceException`.

## Solution

The solution involves initializing the property either in the constructor or assigning a value before using it in the method.