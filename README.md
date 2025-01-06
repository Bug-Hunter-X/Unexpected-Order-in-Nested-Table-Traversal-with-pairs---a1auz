# Lua Nested Table Traversal Issue

This repository demonstrates a potential issue with Lua's `pairs` iterator when traversing nested tables.  The `pairs` iterator does not guarantee a specific order, which can lead to unexpected results, especially when combined with recursive functions.

## Bug Description

The `bug.lua` file contains a function `foo` that recursively iterates through a nested table. Due to the unpredictable order of `pairs`, the processing order of nested tables might not be consistent across different Lua versions or implementations.

## Solution

The `bugSolution.lua` file provides a solution using a different approach to guarantee the processing order of nested tables, such as using `ipairs` for numerically indexed tables or sorting keys explicitly.