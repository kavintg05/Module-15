# Ex. No: 15D - Build a Heap Tree Using Python

## AIM:
To write a Python program to build a heap tree using appropriate Python package and function.

---

## ALGORITHM:

1. **Start the program.**
2. Import the `heapq` module.
3. Define a function `heaptree(H)` that takes a list `H` as input.
4. Use `heapq.heapify(H)` to convert the list into a min-heap.
5. Print the created heap.
6. **End the program.**

---

## PROGRAM:

```
#Reg.NO-212223060119
#Name-Kavindra T G
# Step 2: Import the heapq module
import heapq

# Step 3: Define the heaptree function
def heaptree(H):
    # Step 4: Convert the list into a min-heap
    heapq.heapify(H)
    # Step 5: Print the created heap
    print("Min-Heap:", H)

# Example usage
if __name__ == "__main__":
    # Sample list
    H = [21, 1, 45, 78, 3, 5]
    print("Original List:", H)
    
    # Step 1 and Step 6: Start and end
    heaptree(H)

```

## OUTPUT
![image](https://github.com/user-attachments/assets/75b79891-bc9c-4542-bd8b-d3fd46fc8673)


## RESULT
Thus, the python program to build a heap tree using appropriate Python package and function has been executed and verified successfully.
