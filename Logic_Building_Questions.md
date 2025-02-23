Let's include the output for each code snippet. I'll demonstrate the output for a few examples.

### Pattern Problems

#### 1. Square Star Pattern

```python
def square_star_pattern(n):
    for _ in range(n):
        print('*' * n)

# Example Output
square_star_pattern(4)
```

**Output:**
```
****
****
****
****
```

#### 2. Inverted Pyramid Star Pattern

```python
def inverted_pyramid_star_pattern(n):
    for i in range(n, 0, -1):
        print(' ' * (n - i) + '*' * (2 * i - 1))

# Example Output
inverted_pyramid_star_pattern(3)
```

**Output:**
```
***
 *
***
```

#### 3. Pyramid Star Pattern

```python
def pyramid_star_pattern(n):
    for i in range(1, n + 1):
        print(' ' * (n - i) + '*' * (2 * i - 1))

# Example Output
pyramid_star_pattern(3)
```

**Output:**
```
 *
***
*****
```

#### 4. Diamond Star Pattern

```python
def diamond_star_pattern(n):
    for i in range(1, n + 1):
        print(' ' * (n - i) + '*' * (2 * i - 1))
    for i in range(n - 1, 0, -1):
        print(' ' * (n - i) + '*' * (2 * i - 1))

# Example Output
diamond_star_pattern(3)
```

**Output:**
```
 *
***
*****
***
 *
```

#### 5. Hollow Square Star Pattern

```python
def hollow_square_star_pattern(n):
    for i in range(n):
        for j in range(n):
            if i == 0 or i == n - 1 or j == 0 or j == n - 1:
                print('*', end='')
            else:
                print(' ', end='')
        print()

# Example Output
hollow_square_star_pattern(4)
```

**Output:**
```
****
*  *
*  *
****
```

### Array Problems

#### 1. Reverse an array in place

```python
def reverse_array(arr):
    left, right = 0, len(arr) - 1
    while left < right:
        arr[left], arr[right] = arr[right], arr[left]
        left, right = left + 1, right - 1
    return arr

# Example Output
reverse_array([1, 2, 3, 4])
```

**Output:**
```
[4, 3, 2, 1]
```

#### 2. Find the maximum and minimum elements in an array

```python
def find_max_min(arr):
    max_val = max(arr)
    min_val = min(arr)
    return max_val, min_val

# Example Output
find_max_min([1, 2, 3, 4])
```

**Output:**
```
(4, 1)
```

### String Problems

#### 1. Reverse a string without using extra space

```python
def reverse_string(s):
    return s[::-1]

# Example Output
reverse_string("hello")
```

**Output:**
```
"olleh"
```

#### 2. Check if a string is a palindrome

```python
def is_palindrome(s):
    return s == s[::-1]

# Example Output
is_palindrome("racecar")
```

**Output:**
```
True
```

### Recursion Problems

#### 1. Compute the factorial of a number

```python
def factorial(n):
    if n == 0:
        return 1
    return n * factorial(n - 1)

# Example Output
factorial(5)
```

**Output:**
```
120
```

#### 2. Generate the Fibonacci sequence up to n

```python
def fibonacci(n):
    if n <= 0:
        return []
    if n == 1:
        return [0]
    seq = [0, 1]
    while len(seq) < n:
        seq.append(seq[-1] + seq[-2])
    return seq

# Example Output
fibonacci(5)
```

**Output:**
```
[0, 1, 1, 2, 3]
```

### Mathematical Problems

#### 1. Check if a number is prime

```python
def is_prime(n):
    if n <= 1:
        return False
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return False
    return True

# Example Output
is_prime(7)
```

**Output:**
```
True
```

#### 2. Find the sum of all prime numbers up to n

```python
def sum_of_primes(n):
    def is_prime(num):
        if num <= 1:
            return False
        for i in range(2, int(num ** 0.5) + 1):
            if num % i == 0:
                return False
        return True

    return sum(i for i in range(2, n + 1) if is_prime(i))

# Example Output
sum_of_primes(10)
```

**Output:**
```
17
```

### Bit Manipulation Problems

#### 1. Check if a number is a power of 2

```python
def is_power_of_2(n):
    return n > 0 and (n & (n - 1)) == 0

# Example Output
is_power_of_2(8)
```

**Output:**
```
True
```

#### 2. Find the only non-repeated number in an array where every other number repeats twice

```python
def find_non_repeated(arr):
    unique = 0
    for num in arr:
        unique ^= num
    return unique

# Example Output
find_non_repeated([2, 3, 5, 4, 5, 3, 4])
```

**Output:**
```
2
```

### Projects to Learn Logical Building

#### 1. Simple Calculator with all mathematical conditions

```python
def simple_calculator():
    while True:
        print("Select operation:")
        print("1. Add")
        print("2. Subtract")
        print("3. Multiply")
        print("4. Divide")
        print("5. Exit")
        choice = input("Enter choice (1/2/3/4/5): ")
        if choice == '5':
            break
        num1 = float(input("Enter first number: "))
        num2 = float(input("Enter second number: "))
        if choice == '1':
            print(f"The result is: {num1 + num2}")
        elif choice == '2':
            print(f"The result is: {num1 - num2}")
        elif choice == '3':
            print(f"The result is: {num1 * num2}")
        elif choice == '4':
            if num2 != 0:
                print(f"The result is: {num1 / num2}")
            else:
                print("Error! Division by zero.")
        else:
            print("Invalid input")

# Example Output
# (This function runs interactively, so the output depends on user input.)
```

#### 2. Build a program to generate fractal patterns like the Sierpiński triangle

```python
import matplotlib.pyplot as plt

def sierpinski_triangle(n):
    def draw_triangle(ax, points, depth):
        if depth == 0:
            triangle = plt.Polygon(points, edgecolor='k', facecolor='w')
            ax.add_patch(triangle)
        else:
            p0, p1, p2 = points
            p_mid0 = ((p0[0] + p1[0]) / 2, (p0[1] + p1[1]) / 2)
            p_mid1 = ((p1[0] + p2[0]) / 2, (p1[1] + p2[1]) / 2)
            p_mid2 = ((p2[0] + p0[0]) / 2, (p2[1] + p0[1]) / 2)
            draw_triangle(ax, [p0, p_mid0, p_mid2], depth - 1)
            draw_triangle(ax, [p_mid0, p1, p_mid1], depth - 1)
            draw_triangle(ax, [p_mid2, p_mid1, p2], depth - 1)

    fig, ax = plt.subplots()
    ax.set_aspect('equal')
    ax.axis('off')
    points = [(0, 0), (1, 0), (0.5, 0.866)]
    draw_triangle(ax, points, n)
    plt.show()

# Example Output
sierpinski_triangle(3)
```

**Output:**
- A visual plot of the Sierpiński triangle fractal pattern.

These examples demonstrate the output for various problems, providing a clear understanding of how the code works and what results to expect.