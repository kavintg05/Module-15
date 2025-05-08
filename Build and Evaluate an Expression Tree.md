# Ex. No: 15E - Build and Evaluate an Expression Tree

## AIM:
To write a Python program to build and evaluate the given Expression tree.

---

## ALGORITHM:

1. **Start the program.**
2. Create nodes for operators and operands.
3. Build the expression tree by connecting nodes in the correct hierarchical structure.
4. Define a recursive function `evaluate(root)`:
   - If the node is a number (leaf), return it.
   - Else, recursively evaluate left and right subtrees.
   - Apply the operator at the current node to the results.
5. Return the final result from the root node.
6. **End the program.**

---

## PROGRAM:

```
#Reg.NO-212223060119
#Name-Kavindra T G
WRITE YOUR CODE
class Node:
    def __init__(self, value):
        self.value = value
        self.left = None
        self.right = None

def evaluate(root):
    if root.left is None and root.right is None:
        return int(root.value)
    left_val = evaluate(root.left)
    right_val = evaluate(root.right)
    if root.value == '+':
        return left_val + right_val
    elif root.value == '-':
        return left_val - right_val
    elif root.value == '*':
        return left_val * right_val
    elif root.value == '/':
        return left_val / right_val

root = Node('+')
root.left = Node('3')
right_sub = Node('*')
right_sub.left = Node('+')
right_sub.left.left = Node('5')
right_sub.left.right = Node('9')
right_sub.right = Node('2')
root.right = right_sub

result = evaluate(root)
print("Result of the Expression Tree:", result)

```

## OUTPUT:
![image](https://github.com/user-attachments/assets/16e63d64-4c6d-4643-82ce-6a0f83ee2da9)


## RESULT:
Thus, the python program to build and evaluate the given Expression tree has been executed and verified successfully.
