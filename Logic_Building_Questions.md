

### Pattern Problems

#### 1. Square Star Pattern

```python
def square_star_pattern(n):
    for _ in range(n):
        print('*' * n)

# Explanation: This function prints a square pattern of stars with side length n.
```

#### 2. Inverted Pyramid Star Pattern

```python
def inverted_pyramid_star_pattern(n):
    for i in range(n, 0, -1):
        print(' ' * (n - i) + '*' * (2 * i - 1))

# Explanation: This function prints an inverted pyramid pattern of stars with n levels.
```

#### 3. Pyramid Star Pattern

```python
def pyramid_star_pattern(n):
    for i in range(1, n + 1):
        print(' ' * (n - i) + '*' * (2 * i - 1))

# Explanation: This function prints a pyramid pattern of stars with n levels.
```

#### 4. Diamond Star Pattern

```python
def diamond_star_pattern(n):
    for i in range(1, n + 1):
        print(' ' * (n - i) + '*' * (2 * i - 1))
    for i in range(n - 1, 0, -1):
        print(' ' * (n - i) + '*' * (2 * i - 1))

# Explanation: This function prints a diamond pattern of stars with n levels.
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

# Explanation: This function prints a hollow square pattern of stars with side length n.
```

#### 6. Butterfly Pattern

```python
def butterfly_pattern(n):
    for i in range(1, n + 1):
        print('*' * i + ' ' * (2 * (n - i)) + '*' * i)
    for i in range(n - 1, 0, -1):
        print('*' * i + ' ' * (2 * (n - i)) + '*' * i)

# Explanation: This function prints a butterfly pattern of stars with n levels.
```

#### 7. Downward Triangle Star Pattern

```python
def downward_triangle_star_pattern(n):
    for i in range(n, 0, -1):
        print('*' * i)

# Explanation: This function prints a downward triangle pattern of stars with n levels.
```

#### 8. Hollow Diamond Star Pattern

```python
def hollow_diamond_star_pattern(n):
    for i in range(n):
        for j in range(n - i - 1):
            print(' ', end='')
        for j in range(2 * i + 1):
            if j == 0 or j == 2 * i:
                print('*', end='')
            else:
                print(' ', end='')
        print()
    for i in range(n - 2, -1, -1):
        for j in range(n - i - 1):
            print(' ', end='')
        for j in range(2 * i + 1):
            if j == 0 or j == 2 * i:
                print('*', end='')
            else:
                print(' ', end='')
        print()

# Explanation: This function prints a hollow diamond pattern of stars with n levels.
```

#### 9. Cross Star Pattern

```python
def cross_star_pattern(n):
    for i in range(n):
        for j in range(n):
            if i == j or i == n - j - 1:
                print('*', end='')
            else:
                print(' ', end='')
        print()

# Explanation: This function prints a cross pattern of stars with side length n.
```

#### 10. Hollow Pyramid Star Pattern

```python
def hollow_pyramid_star_pattern(n):
    for i in range(n):
        for j in range(n - i - 1):
            print(' ', end='')
        for j in range(2 * i + 1):
            if j == 0 or j == 2 * i or i == n - 1:
                print('*', end='')
            else:
                print(' ', end='')
        print()

# Explanation: This function prints a hollow pyramid pattern of stars with n levels.
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

# Explanation: This function reverses an array in place by swapping elements from the ends towards the center.
```

#### 2. Find the maximum and minimum elements in an array

```python
def find_max_min(arr):
    max_val = max(arr)
    min_val = min(arr)
    return max_val, min_val

# Explanation: This function finds the maximum and minimum elements in an array using Python's built-in max and min functions.
```

#### 3. Rotate an array to the right by k steps

```python
def rotate_array(arr, k):
    n = len(arr)
    k = k % n
    arr[:] = arr[-k:] + arr[:-k]
    return arr

# Explanation: This function rotates an array to the right by k steps by slicing and concatenating the array.
```

#### 4. Find the second largest element in an array

```python
def second_largest(arr):
    unique_arr = list(set(arr))
    unique_arr.sort()
    return unique_arr[-2]

# Explanation: This function finds the second largest element in an array by removing duplicates, sorting, and returning the second last element.
```

#### 5. Check if two arrays are rotations of each other

```python
def are_rotations(arr1, arr2):
    if len(arr1) != len(arr2):
        return False
    combined = arr1 + arr1
    return any(combined[i:i+len(arr1)] == arr2 for i in range(len(arr1)))

# Explanation: This function checks if two arrays are rotations of each other by concatenating one array with itself and checking for subarray equality.
```

#### 6. Find all pairs in an array whose sum equals a target

```python
def find_pairs(arr, target):
    pairs = []
    seen = set()
    for num in arr:
        complement = target - num
        if complement in seen:
            pairs.append((complement, num))
        seen.add(num)
    return pairs

# Explanation: This function finds all pairs in an array whose sum equals a target by using a set to track seen elements.
```

#### 7. Merge two sorted arrays into a single sorted array

```python
def merge_sorted_arrays(arr1, arr2):
    merged = []
    i, j = 0, 0
    while i < len(arr1) and j < len(arr2):
        if arr1[i] < arr2[j]:
            merged.append(arr1[i])
            i += 1
        else:
            merged.append(arr2[j])
            j += 1
    merged.extend(arr1[i:])
    merged.extend(arr2[j:])
    return merged

# Explanation: This function merges two sorted arrays into a single sorted array by comparing elements and appending the smaller one.
```

#### 8. Move all zeros in an array to the end

```python
def move_zeros(arr):
    non_zero_elements = [num for num in arr if num != 0]
    zero_count = len(arr) - len(non_zero_elements)
    return non_zero_elements + [0] * zero_count

# Explanation: This function moves all zeros in an array to the end by separating non-zero elements and appending zeros at the end.
```

#### 9. Find the length of the longest subarray with a given sum

```python
def longest_subarray_with_sum(arr, target_sum):
    sum_map = {}
    current_sum = 0
    max_length = 0
    for i in range(len(arr)):
        current_sum += arr[i]
        if current_sum == target_sum:
            max_length = i + 1
        if current_sum - target_sum in sum_map:
            max_length = max(max_length, i - sum_map[current_sum - target_sum])
        if current_sum not in sum_map:
            sum_map[current_sum] = i
    return max_length

# Explanation: This function finds the length of the longest subarray with a given sum using a hash map to store cumulative sums.
```

#### 10. Determine if an array contains a subarray with a sum of zero

```python
def has_zero_sum_subarray(arr):
    sum_set = set()
    current_sum = 0
    for num in arr:
        current_sum += num
        if current_sum == 0 or current_sum in sum_set:
            return True
        sum_set.add(current_sum)
    return False

# Explanation: This function determines if an array contains a subarray with a sum of zero using a set to track cumulative sums.
```

### String Problems

#### 1. Reverse a string without using extra space

```python
def reverse_string(s):
    return s[::-1]

# Explanation: This function reverses a string using Python's slicing feature.
```

#### 2. Check if a string is a palindrome

```python
def is_palindrome(s):
    return s == s[::-1]

# Explanation: This function checks if a string is a palindrome by comparing it to its reverse.
```

#### 3. Find the first non-repeating character in a string

```python
def first_non_repeating_char(s):
    char_count = {}
    for char in s:
        char_count[char] = char_count.get(char, 0) + 1
    for char in s:
        if char_count[char] == 1:
            return char
    return None

# Explanation: This function finds the first non-repeating character in a string by counting character occurrences.
```

#### 4. Count the frequency of each character in a string

```python
def char_frequency(s):
    freq = {}
    for char in s:
        freq[char] = freq.get(char, 0) + 1
    return freq

# Explanation: This function counts the frequency of each character in a string using a dictionary.
```

#### 5. Check if two strings are anagrams

```python
def are_anagrams(s1, s2):
    return sorted(s1) == sorted(s2)

# Explanation: This function checks if two strings are anagrams by sorting and comparing them.
```

#### 6. Implement a basic string compression algorithm

```python
def compress_string(s):
    compressed = []
    count = 1
    for i in range(1, len(s)):
        if s[i] == s[i - 1]:
            count += 1
        else:
            compressed.append(s[i - 1] + str(count))
            count = 1
    compressed.append(s[-1] + str(count))
    return ''.join(compressed)

# Explanation: This function implements a basic string compression algorithm by counting consecutive characters.
```

#### 7. Find the longest common prefix among a set of strings

```python
def longest_common_prefix(strs):
    if not strs:
        return ""
    prefix = strs[0]
    for s in strs[1:]:
        while s[:len(prefix)] != prefix:
            prefix = prefix[:-1]
            if not prefix:
                return ""
    return prefix

# Explanation: This function finds the longest common prefix among a set of strings by comparing characters from the beginning.
```

#### 8. Replace all spaces in a string with %20

```python
def replace_spaces(s):
    return s.replace(' ', '%20')

# Explanation: This function replaces all spaces in a string with '%20' using Python's replace method.
```

#### 9. Find the longest palindromic substring

```python
def longest_palindromic_substring(s):
    n = len(s)
    if n == 0:
        return ""
    start, max_length = 0, 1
    for i in range(n):
        if i - max_length >= 1 and s[i - max_length - 1:i + 1] == s[i - max_length - 1:i + 1][::-1]:
            start = i - max_length - 1
            max_length += 2
            continue
        if s[i - max_length:i + 1] == s[i - max_length:i + 1][::-1]:
            start = i - max_length
            max_length += 1
    return s[start:start + max_length]

# Explanation: This function finds the longest palindromic substring by expanding around each character.
```

#### 10. Print all permutations of a string

```python
def permute_string(s):
    from itertools import permutations
    return [''.join(p) for p in permutations(s)]

# Explanation: This function prints all permutations of a string using Python's itertools.permutations.
```

### Recursion Problems

#### 1. Compute the factorial of a number

```python
def factorial(n):
    if n == 0:
        return 1
    return n * factorial(n - 1)

# Explanation: This function computes the factorial of a number using recursion.
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

# Explanation: This function generates the Fibonacci sequence up to n using iteration.
```

#### 3. Solve the Tower of Hanoi for n disks

```python
def tower_of_hanoi(n, source, auxiliary, target):
    if n == 1:
        print(f"Move disk 1 from {source} to {target}")
        return
    tower_of_hanoi(n - 1, source, target, auxiliary)
    print(f"Move disk {n} from {source} to {target}")
    tower_of_hanoi(n - 1, auxiliary, source, target)

# Explanation: This function solves the Tower of Hanoi problem using recursion.
```

#### 4. Print all subsets of a given array

```python
def print_subsets(arr):
    def backtrack(start, path):
        print(path)
        for i in range(start, len(arr)):
            backtrack(i + 1, path + [arr[i]])
    backtrack(0, [])

# Explanation: This function prints all subsets of a given array using backtracking.
```

#### 5. Find the nth term of a geometric progression using recursion

```python
def geometric_progression(a, r, n):
    if n == 1:
        return a
    return r * geometric_progression(a, r, n - 1)

# Explanation: This function finds the nth term of a geometric progression using recursion.
```

#### 6. Solve the N-Queens problem for a chessboard of size n x n

```python
def solve_n_queens(n):
    def is_safe(board, row, col):
        for i in range(row):
            if board[i] == col or abs(board[i] - col) == abs(i - row):
                return False
        return True

    def solve(board, row):
        if row == n:
            solutions.append(board[:])
            return
        for col in range(n):
            if is_safe(board, row, col):
                board[row] = col
                solve(board, row + 1)
                board[row] = -1

    solutions = []
    board = [-1] * n
    solve(board, 0)
    return solutions

# Explanation: This function solves the N-Queens problem using backtracking.
```

#### 7. Generate all valid combinations of n pairs of parentheses

```python
def generate_parentheses(n):
    def backtrack(s, left, right):
        if len(s) == 2 * n:
            combinations.append(s)
            return
        if left < n:
            backtrack(s + '(', left + 1, right)
        if right < left:
            backtrack(s + ')', left, right + 1)

    combinations = []
    backtrack('', 0, 0)
    return combinations

# Explanation: This function generates all valid combinations of n pairs of parentheses using backtracking.
```

#### 8. Perform binary search recursively

```python
def binary_search(arr, target, low, high):
    if low > high:
        return -1
    mid = (low + high) // 2
    if arr[mid] == target:
        return mid
    elif arr[mid] < target:
        return binary_search(arr, target, mid + 1, high)
    else:
        return binary_search(arr, target, low, mid - 1)

# Explanation: This function performs binary search recursively to find a target element in a sorted array.
```

#### 9. Find the greatest common divisor (GCD) of two numbers using recursion

```python
def gcd(a, b):
    if b == 0:
        return a
    return gcd(b, a % b)

# Explanation: This function finds the GCD of two numbers using the Euclidean algorithm and recursion.
```

#### 10. Count the number of ways to climb n stairs with steps of 1 or 2

```python
def climb_stairs(n):
    if n == 0 or n == 1:
        return 1
    return climb_stairs(n - 1) + climb_stairs(n - 2)

# Explanation: This function counts the number of ways to climb n stairs with steps of 1 or 2 using recursion.
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

# Explanation: This function checks if a number is prime by testing divisibility up to the square root of the number.
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

# Explanation: This function finds the sum of all prime numbers up to n by checking each number for primality.
```

#### 3. Determine the number of trailing zeros in the factorial of a number

```python
def trailing_zeros_in_factorial(n):
    count = 0
    power_of_5 = 5
    while n >= power_of_5:
        count += n // power_of_5
        power_of_5 *= 5
    return count

# Explanation: This function determines the number of trailing zeros in the factorial of a number by counting the factors of 5.
```

#### 4. Calculate the sum of digits of a number until it becomes a single digit

```python
def sum_of_digits(n):
    while n >= 10:
        n = sum(int(digit) for digit in str(n))
    return n

# Explanation: This function calculates the sum of digits of a number until it becomes a single digit by repeatedly summing the digits.
```

#### 5. Solve modular exponentiation efficiently

```python
def modular_exponentiation(base, exp, mod):
    result = 1
    base = base % mod
    while exp > 0:
        if exp % 2 == 1:
            result = (result * base) % mod
        exp = exp >> 1
        base = (base * base) % mod
    return result

# Explanation: This function solves modular exponentiation efficiently using the method of exponentiation by squaring.
```

#### 6. Find all prime factors of a number

```python
def prime_factors(n):
    factors = []
    while n % 2 == 0:
        factors.append(2)
        n //= 2
    for i in range(3, int(n ** 0.5) + 1, 2):
        while n % i == 0:
            factors.append(i)
            n //= i
    if n > 2:
        factors.append(n)
    return factors

# Explanation: This function finds all prime factors of a number by dividing it by its smallest factors.
```

#### 7. Check if a number is an Armstrong number

```python
def is_armstrong(n):
    num_str = str(n)
    power = len(num_str)
    return n == sum(int(digit) ** power for digit in num_str)

# Explanation: This function checks if a number is an Armstrong number by comparing it to the sum of its digits raised to the power of the number of digits.
```

#### 8. Print the first n perfect numbers

```python
def perfect_numbers(n):
    def is_perfect(num):
        return num == sum(i for i in range(1, num) if num % i == 0)

    count, num = 0, 2
    perfects = []
    while count < n:
        if is_perfect(num):
            perfects.append(num)
            count += 1
        num += 1
    return perfects

# Explanation: This function prints the first n perfect numbers by checking each number for perfection.
```

#### 9. Determine if a number is a palindrome

```python
def is_number_palindrome(n):
    return str(n) == str(n)[::-1]

# Explanation: This function determines if a number is a palindrome by comparing it to its reverse.
```

#### 10. Compute the nth Fibonacci number iteratively

```python
def fibonacci_number(n):
    if n <= 0:
        return 0
    elif n == 1:
        return 1
    a, b = 0, 1
    for _ in range(2, n + 1):
        a, b = b, a + b
    return b

# Explanation: This function computes the nth Fibonacci number iteratively by updating two variables.
```

### Bit Manipulation Problems

#### 1. Check if a number is a power of 2

```python
def is_power_of_2(n):
    return n > 0 and (n & (n - 1)) == 0

# Explanation: This function checks if a number is a power of 2 by using bitwise AND with its predecessor.
```

#### 2. Find the only non-repeated number in an array where every other number repeats twice

```python
def find_non_repeated(arr):
    unique = 0
    for num in arr:
        unique ^= num
    return unique

# Explanation: This function finds the only non-repeated number in an array using XOR to cancel out repeated numbers.
```

#### 3. Count the number of 1 bits in a number

```python
def count_one_bits(n):
    return bin(n).count('1')

# Explanation: This function counts the number of 1 bits in a number by converting it to binary and counting '1's.
```

#### 4. Toggle the kth bit of a number

```python
def toggle_kth_bit(n, k):
    return n ^ (1 << k)

# Explanation: This function toggles the kth bit of a number using XOR with a shifted 1.
```

#### 5. Find the XOR of all elements in an array

```python
def xor_of_array(arr):
    result = 0
    for num in arr:
        result ^= num
    return result

# Explanation: This function finds the XOR of all elements in an array by iteratively applying XOR.
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

# Explanation: This function implements a simple calculator that performs basic arithmetic operations.
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

# Explanation: This function generates the Sierpiński triangle fractal pattern using recursive drawing.
```

#### 3. Implement a matrix multiplication program

```python
def matrix_multiply(A, B):
    if len(A[0]) != len(B):
        raise ValueError("Number of columns in A must be equal to number of rows in B")
    result = [[0] * len(B[0]) for _ in range(len(A))]
    for i in range(len(A)):
        for j in range(len(B[0])):
            for k in range(len(B)):
                result[i][j] += A[i][k] * B[k][j]
    return result

# Explanation: This function implements matrix multiplication by iterating through the rows and columns of the matrices.
```

#### 4. Create a Sudoku solver

```python
def solve_sudoku(board):
    def is_valid(board, row, col, num):
        for i in range(9):
            if board[row][i] == num or board[i][col] == num:
                return False
        start_row, start_col = 3 * (row // 3), 3 * (col // 3)
        for i in range(start_row, start_row + 3):
            for j in range(start_col, start_col + 3):
                if board[i][j] == num:
                    return False
        return True

    def solve(board):
        for row in range(9):
            for col in range(9):
                if board[row][col] == 0:
                    for num in range(1, 10):
                        if is_valid(board, row, col, num):
                            board[row][col] = num
                            if solve(board):
                                return True
                            board[row][col] = 0
                    return False
        return True

    solve(board)
    return board

# Explanation: This function solves a Sudoku puzzle using backtracking and validation checks.
```

#### 5. Develop a program to check plagiarism in documents by comparing substrings

```python
def check_plagiarism(doc1, doc2, k):
    def get_substrings(doc, k):
        return {doc[i:i+k] for i in range(len(doc) - k + 1)}

    substrings1 = get_substrings(doc1, k)
    substrings2 = get_substrings(doc2, k)
    common_substrings = substrings1.intersection(substrings2)
    return len(common_substrings) / len(substrings1)

# Explanation: This function checks for plagiarism by comparing substrings of length k between two documents.
```

#### 6. Create a maze solver using recursion and backtracking

```python
def solve_maze(maze):
    def is_safe(maze, x, y):
        return 0 <= x < len(maze) and 0 <= y < len(maze[0]) and maze[x][y] == 1

    def solve(maze, x, y, solution):
        if x == len(maze) - 1 and y == len(maze[0]) - 1:
            solution[x][y] = 1
            return True
        if is_safe(maze, x, y):
            solution[x][y] = 1
            if solve(maze, x + 1, y, solution):
                return True
            if solve(maze, x, y + 1, solution):
                return True
            solution[x][y] = 0
            return False
        return False

    solution = [[0] * len(maze[0]) for _ in range(len(maze))]
    if solve(maze, 0, 0, solution):
        return solution
    else:
        return None

# Explanation: This function solves a maze using recursion and backtracking to find a path from the start to the end.
```

#### 7. Build a basic file compression algorithm using bit-level operations

```python
def compress_file(data):
    compressed = []
    for char in data:
        binary = format(ord(char), '08b')
        compressed.append(binary)
    return ''.join(compressed)

def decompress_file(compressed):
    decompressed = []
    for i in range(0, len(compressed), 8):
        byte = compressed[i:i+8]
        char = chr(int(byte, 2))
        decompressed.append(char)
    return ''.join(decompressed)

# Explanation: This function implements a basic file compression algorithm using bit-level operations to convert characters to binary and back.
```

