# LeetCode 9: Palindrome Number

## Problem Statement

Given an integer `x`, return `true` if `x` is a palindrome and `false` otherwise.

A palindrome number reads the same forward and backward.

### Example 1
Input:
```text
x = 121
```
Output:
```text
true
```

### Example 2
Input:
```text
x = -121
```
Output:
```text
false
```

### Example 3
Input:
```text
x = 10
```
Output:
```text
false
```

## Approach

1. Negative numbers cannot be palindromes.
2. Store the original number.
3. Reverse the digits of the number.
4. Compare the reversed number with the original number.
5. Return `true` if they are equal; otherwise, return `false`.

## Java Solution

```java
class Solution {
    public boolean isPalindrome(int x) {
        if (x < 0) {
            return false;
        }

        int original = x;
        long reverse = 0;

        while (x != 0) {
            reverse = reverse * 10 + x % 10;
            x /= 10;
        }

        return original == reverse;
    }
}
```

## Complexity Analysis

- **Time Complexity:** O(log n)
- **Space Complexity:** O(1)

## Tags

`Math` `Palindrome` `Number Manipulation`
