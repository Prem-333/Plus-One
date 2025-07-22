# Plus-One
Plus One – LeetCode Problem
📌 Problem Statement
You are given a non-empty array of digits representing a non-negative integer. The digits are stored such that the most significant digit is at the head of the list, and each element in the array contains a single digit.

Increment the large integer by one and return the resulting array of digits.

✅ Example 1:
Input:

ini
Copy
Edit
digits = [1, 2, 3]
Output:

csharp
Copy
Edit
[1, 2, 4]
Explanation:
123 + 1 = 124

✅ Example 2:
Input:

ini
Copy
Edit
digits = [9, 9, 9]
Output:

csharp
Copy
Edit
[1, 0, 0, 0]
🔍 Approach
Start from the last digit.

Add 1 to it.

If it becomes 10, set it to 0 and carry over.

Repeat until there is no carry.

If the entire list is processed and carry remains, insert 1 at the front.

🕒 Complexity
Time Complexity: O(n)

Space Complexity: O(1) (in-place modification)

💻 Code (Python)
python
Copy
Edit
class Solution:
    def plusOne(self, digits):
        n = len(digits)
        for i in range(n - 1, -1, -1):
            digits[i] += 1
            digits[i] %= 10
            if digits[i] != 0:
                return digits
        return [1] + digits
🔗 Related Topics
Arrays

Math

