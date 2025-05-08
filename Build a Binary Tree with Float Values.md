# Ex. No: 15A - Build a Binary Tree with Float Values

## AIM:
To write a Python program to build a binary tree with a root, left, and right node using floating-point values.

---

## ALGORITHM:

1. **Start the program.**
2. **Import** the `Node` class from the `binarytree` module.
3. **Create a root node** using the `Node` class and assign a floating-point value.
4. **Create left and right child nodes** for the root with float values.
5. **Convert the tree** to a list and print the list of nodes.
6. **End the program.**

---

## PYTHON PROGRAM

```
#Reg.NO-212223060119
#Name-Kavindra T G
ENTER YOUR CODE
from binarytree import Node

class FloatNode:
    def __init__(self, value):
        self.value = float(value)
        self.left = None
        self.right = None

def tree_to_list(root):
    result = []
    def traverse(node):
        if node:
            result.append(node.value)
            traverse(node.left)
            traverse(node.right)
    traverse(root)
    return result

if __name__ == "__main__":
    root = FloatNode(10.5)
    root.left = FloatNode(5.25)
    root.right = FloatNode(15.75)

    nodes_list = tree_to_list(root)
    print("List of nodes in the tree:", nodes_list)

```

## OUTPUT
![image](https://github.com/user-attachments/assets/a95da670-befd-49c2-8fc8-4ce6579365f3)


## RESULT
Thus, the python program to build a binary tree with a root, left, and right node using floating-point values has been executed and verified successfully.
