# Ex. No: 15B - Build a Binary Search Tree Using Built-in Function

## AIM:
To write a Python program to build a binary search tree using a built-in function.

---

## ALGORITHM:

1. **Start the program.**
2. Define `_build_bst_from_sorted_values(sorted_values)` to recursively build a binary search tree (BST) from a sorted list.
3. Define `left_subtree(l)` to print the left subtree of the BST.
4. Take user input for the number of elements and store the values in a list `a`.
5. Sort the list and pass it to `_build_bst_from_sorted_values()` to construct the BST.
6. Print the postorder traversal of the BST.
7. Call `left_subtree(l)` to print the left subtree.
8. Check whether the tree is a binary search tree using the `is_bst` property.
9. **End the program.**

---

## PROGRAM:

```
ENTER YOUR CODE
from dataclasses import dataclass
from typing import Optional, List

@dataclass
class Node:
    value: int
    left: Optional['Node'] = None
    right: Optional['Node'] = None

def _build_bst_from_sorted_values(sorted_values: List[int]) -> Optional[Node]:
    if not sorted_values:
        return None
    mid = len(sorted_values) // 2
    root = Node(sorted_values[mid])
    root.left = _build_bst_from_sorted_values(sorted_values[:mid])
    root.right = _build_bst_from_sorted_values(sorted_values[mid+1:])
    return root

def left_subtree(root: Optional[Node]):
    if root and root.left:
        print("Left Subtree:")
        postorder_traversal(root.left)
    else:
        print("No Left Subtree")

def postorder_traversal(root: Optional[Node]):
    if root:
        postorder_traversal(root.left)
        postorder_traversal(root.right)
        print(root.value, end=' ')

def is_bst(root: Optional[Node], min_val=float('-inf'), max_val=float('inf')) -> bool:
    if root is None:
        return True
    if not (min_val < root.value < max_val):
        return False
    return (is_bst(root.left, min_val, root.value) and
            is_bst(root.right, root.value, max_val))

if __name__ == "__main__":
    n = int(input("Enter the number of elements: "))
    a = []
    for _ in range(n):
        a.append(int(input("Enter value: ")))
    a.sort()
    root = _build_bst_from_sorted_values(a)
    print("\nPostorder Traversal of the BST:")
    postorder_traversal(root)
    print("\n")
    left_subtree(root)
    print("\nIs the tree a Binary Search Tree?", is_bst(root))

```

## OUTPUT
![image](https://github.com/user-attachments/assets/c6669741-6c1b-491c-a9c9-c8426f9fb0e0)


## RESULT
Thus, the python program to build a binary search tree using a built-in function has been executed and verified successfully.
