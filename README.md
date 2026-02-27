📘 Sum of List Elements Using Recursion (Python)

📌 Overview

This Python program calculates the sum of all elements in a list using a recursive approach.

Recursion allows a function to solve a problem by breaking it down into smaller subproblems of the same type.

⚙️ Source Code
def sum_list(lst):
    if len(lst) == 0:
        return 0
    else:
        return lst[0] + sum_list(lst[1:])

print(sum_list([1,2,3,4]))
🧠 How It Works
1️⃣ Function Definition
def sum_list(lst):

Defines a function sum_list that takes a list lst as input.

2️⃣ Base Case
if len(lst) == 0:
    return 0

Stops recursion when the list becomes empty.

Returns 0 because the sum of an empty list is 0.

3️⃣ Recursive Case
return lst[0] + sum_list(lst[1:])

lst[0] → First element of the list.

lst[1:] → Remaining list (excluding first element).

The function keeps calling itself with a smaller list.

Each recursive call adds the first element to the sum of the remaining list.

🔄 Execution Example

For:

sum_list([1,2,3,4])

The recursive breakdown:

sum_list([1,2,3,4])
= 1 + sum_list([2,3,4])
= 1 + 2 + sum_list([3,4])
= 1 + 2 + 3 + sum_list([4])
= 1 + 2 + 3 + 4 + sum_list([])
= 1 + 2 + 3 + 4 + 0
= 10
▶️ Output
10
🔑 Key Concepts Demonstrated

Recursive functions

Base case handling

List slicing (lst[1:])

Breaking problems into smaller subproblems

⏱️ Time & Space Complexity

Time Complexity: O(n²)
(Because list slicing creates a new list each time)

Space Complexity: O(n)
(Due to recursive call stack)

🚀 More Efficient Alternative (Iterative)
def sum_list(lst):
    total = 0
    for num in lst:
        total += num
    return total

Or using Python built-in:

sum([1,2,3,4])
📚 Learning Outcomes

After understanding this program, you should be able to:

Write recursive functions for lists

Identify base and recursive cases

Understand performance trade-offs

Compare recursive vs iterative solutions

<img width="733" height="708" alt="image" src="https://github.com/user-attachments/assets/214283a8-7f55-4dfc-8e6c-dbe1f771605c" />
