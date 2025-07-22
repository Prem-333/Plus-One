# Plus-One
Problem Description
You are given a non-empty array of digits representing a non-negative integer, where each element in the array represents a single digit of the number. The most significant digit is at the beginning of the array, and the least significant digit is at the end. The task is to add one to this integer and return the result as an array of digits.

Example
Input:
digits = [1, 2, 3]
Output:
[1, 2, 4]
Explanation:
123 + 1 = 124

Approach
Start from the last digit and add 1.

If the digit becomes 10, set it to 0 and carry over to the previous digit.

Continue until:

No carry remains, or

All digits processed → prepend 1 if carry remains.

Algorithm
Traverse the list in reverse order.

Add 1 to the last digit.

Handle carry by setting digit to 0 if it becomes 10.

If all digits become 0, insert 1 at the start.

Return the modified list.

Complexity
Time Complexity: O(n) (traverse digits once)

Space Complexity: O(1) (in-place, ignoring output list)

