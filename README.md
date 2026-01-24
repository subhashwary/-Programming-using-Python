# Programming-using-Python
Python codes for practice

1. Check Even or Odd: Determine if a number is divisible by 2.
num = int(input("Enter a number: "))
if num % 2 == 0:
    print("Even")
else:
    print("Odd")

2. Factorial Calculation: Find the product of all positive integers up to \(n\) using recursion

def factorial(n):
    return 1 if n == 0 else n * factorial(n - 1)

print(factorial(5))  # Output: 120

Reverse a String: Use slicing to reverse text.
my_str = "Python"
print(my_str[::-1])  # Output: nohtyP

3. Fibonacci Sequence: Generate the first \(n\) terms of the sequence.
def fibonacci(n):
    seq = [0, 1]
    for _ in range(2, n):
        seq.append(seq[-1] + seq[-2])
    return seq[:n]

print(fibonacci(7)) # Output: [0, 1, 1, 2, 3, 5, 8]

4. Matrix Transpose: Convert rows into columns using list comprehension.
matrix = [[1, 2], [3, 4], [5, 6]]
transpose = [[row[i] for row in matrix] for i in range(len(matrix[0]))]
Result: [[1, 3, 5], [2, 4, 6]]

5. List Flattening: Convert a nested list into a single-level list.
def flatten(nested):
    flat = []
    for item in nested:
        if isinstance(item, list):
            flat.extend(flatten(item))
        else:
            flat.append(item)
    return flat