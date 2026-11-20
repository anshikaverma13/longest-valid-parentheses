# Longest Valid Parentheses

A Python solution to find the length of the longest valid (well-formed) parentheses substring in a given string containing only `(` and `)`.

## Problem Statement

Given a string `s` containing only opening and closing parentheses, return the length of the longest valid parentheses substring.

### Examples

| Input | Output |
|---|---:|
| `"(()"` | `2` |
| `")()())"` | `4` |
| `""` | `0` |

## Approach: Stack

The solution uses a stack to track the indices of unmatched parentheses.

- Initialize the stack with `-1` as the base index.
- Push the index whenever an opening parenthesis `(` is encountered.
- When a closing parenthesis `)` is encountered, pop the stack.
- If the stack becomes empty, push the current index as the new boundary.
- Otherwise, calculate the valid substring length using the difference between the current index and the index at the top of the stack.
- Keep track of the maximum length found.

## Solution

See [`solution.py`](solution.py) for the complete Python implementation.

## Complexity Analysis

- **Time Complexity:** O(n) — The string is traversed once.
- **Space Complexity:** O(n) — The stack can store up to n indices.

## How to Run

Make sure Python 3 is installed, then run:

```bash
python solution.py
```

## Test Cases

```text
Input:  "(()"
Output: 2

Input:  ")()())"
Output: 4

Input:  ""
Output: 0

Input:  "()(())"
Output: 6
```

---

**Language:** Python 3  
**Algorithm:** Stack  
**Problem:** Longest Valid Parentheses
