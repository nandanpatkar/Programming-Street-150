
### Pattern Problems

#### 1. Square Star Pattern

```python
def square_star_pattern(n):
    for _ in range(n):
        print('*' * n)

square_star_pattern(5)
```

**Explanation:** This code prints a square pattern of stars. The outer loop runs `n` times to print `n` rows, and each row consists of `n` stars.

**Output:**
```
*****
*****
*****
*****
*****
```

#### 2. Inverted Pyramid Star Pattern

```python
def inverted_pyramid_star_pattern(n):
    for i in range(n, 0, -1):
        print(' ' * (n - i) + '*' * (2 * i - 1))

inverted_pyramid_star_pattern(5)
```

**Explanation:** This code prints an inverted pyramid pattern. The outer loop runs from `n` to `1`, and each row consists of spaces followed by stars.

**Output:**
```
*********
 *******
  *****
   ***
    *
```

#### 3. Pyramid Star Pattern

```python
def pyramid_star_pattern(n):
    for i in range(1, n + 1):
        print(' ' * (n - i) + '*' * (2 * i - 1))

pyramid_star_pattern(5)
```

**Explanation:** This code prints a pyramid pattern. The outer loop runs from `1` to `n`, and each row consists of spaces followed by stars.

**Output:**
```
    *
   ***
  *****
 *******
*********
```

#### 4. Diamond Star Pattern

```python
def diamond_star_pattern(n):
    for i in range(1, n + 1):
        print(' ' * (n - i) + '*' * (2 * i - 1))
    for i in range(n - 1, 0, -1):
        print(' ' * (n - i) + '*' * (2 * i - 1))

diamond_star_pattern(5)
```

**Explanation:** This code prints a diamond pattern by combining the pyramid and inverted pyramid patterns.

**Output:**
```
    *
   ***
  *****
 *******
*********
 *******
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

hollow_square_star_pattern(5)
```

**Explanation:** This code prints a hollow square pattern. It prints stars at the borders and spaces inside.

**Output:**
```
*****
*   *
*   *
*   *
*****
```

#### 6. Butterfly Pattern

```python
def butterfly_pattern(n):
    for i in range(1, n + 1):
        print('*' * i + ' ' * (2 * (n - i)) + '*' * i)
    for i in range(n - 1, 0, -1):
        print('*' * i + ' ' * (2 * (n - i)) + '*' * i)

butterfly_pattern(5)
```

**Explanation:** This code prints a butterfly pattern by combining two mirrored right-angled triangles.

**Output:**
```
*        *
**      **
***    ***
****  ****
**********
****  ****
***    ***
**      **
*        *
```

#### 7. Downward Triangle Star Pattern

```python
def downward_triangle_star_pattern(n):
    for i in range(n, 0, -1):
        print('*' * i)

downward_triangle_star_pattern(5)
```

**Explanation:** This code prints a downward triangle pattern. The outer loop runs from `n` to `1`, and each row consists of `i` stars.

**Output:**
```
*****
****
***
**
*
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

hollow_diamond_star_pattern(5)
```

**Explanation:** This code prints a hollow diamond pattern by combining hollow pyramid and inverted hollow pyramid patterns.

**Output:**
```
    *
   * *
  *   *
 *     *
*       *
 *     *
  *   *
   * *
    *
```

#### 9. Cross Star Pattern

```python
def cross_star_pattern(n):
    for i in range(n):
        for j in range(n):
            if i == j or i + j == n - 1:
                print('*', end='')
            else:
                print(' ', end='')
        print()

cross_star_pattern(5)
```

**Explanation:** This code prints a cross pattern. It prints stars at the diagonals and spaces elsewhere.

**Output:**
```
*   *
 * *
  *
 * *
*   *
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

hollow_pyramid_star_pattern(5)
```

**Explanation:** This code prints a hollow pyramid pattern. It prints stars at the borders and spaces inside.

**Output:**
```
    *
   * *
  *   *
 *     *
*********
```

### Array Problems

#### 1. Reverse an array in place

```python
def reverse_array(arr):
    left, right = 0, len(arr) - 1
    while left < right:
        arr[left], arr[right] = arr[right], arr[left]
        left += 1
        right -= 1
    return arr

reverse_array([1, 2, 3, 4, 5])
```

**Explanation:** This code reverses an array in place by swapping elements from the start and end towards the center.

**Output:**
```
[5, 4, 3, 2, 1]
```

#### 2. Find the maximum and minimum elements in an array

```python
def find_max_min(arr):
    max_val = max(arr)
    min_val = min(arr)
    return max_val, min_val

find_max_min([1, 2, 3, 4, 5])
```

**Explanation:** This code finds the maximum and minimum elements in an array using the `max` and `min` functions.

**Output:**
```
(5, 1)
```

#### 3. Rotate an array to the right by k steps

```python
def rotate_array(arr, k):
    n = len(arr)
    k = k % n
    return arr[-k:] + arr[:-k]

rotate_array([1, 2, 3, 4, 5], 2)
```

**Explanation:** This code rotates an array to the right by `k` steps by slicing and concatenating the array.

**Output:**
```
[4, 5, 1, 2, 3]
```

#### 4. Find the second largest element in an array

```python
def second_largest(arr):
    unique_arr = list(set(arr))
    unique_arr.sort()
    return unique_arr[-2]

second_largest([1, 2, 3, 4, 5])
```

**Explanation:** This code finds the second largest element by removing duplicates, sorting the array, and returning the second last element.

**Output:**
```
4
```

#### 5. Check if two arrays are rotations of each other

```python
def are_rotations(arr1, arr2):
    if len(arr1) != len(arr2):
        return False
    combined = arr1 + arr1
    return any(combined[i:i+len(arr1)] == arr2 for i in range(len(arr1)))

are_rotations([1, 2, 3, 4, 5], [3, 4, 5, 1, 2])
```

**Explanation:** This code checks if two arrays are rotations of each other by combining the first array with itself and checking for the presence of the second array.

**Output:**
```
True
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

find_pairs([1, 2, 3, 4, 5], 5)
```

**Explanation:** This code finds all pairs in an array whose sum equals a target by using a set to track seen numbers.

**Output:**
```
[(1, 4), (2, 3)]
```

#### 7. Merge two sorted arrays into a single sorted array

```python
def merge_sorted_arrays(arr1, arr2):
    return sorted(arr1 + arr2)

merge_sorted_arrays([1, 3, 5], [2, 4, 6])
```

**Explanation:** This code merges two sorted arrays into a single sorted array using the `sorted` function.

**Output:**
```
[1, 2, 3, 4, 5, 6]
```

#### 8. Move all zeros in an array to the end

```python
def move_zeros(arr):
    non_zeros = [num for num in arr if num != 0]
    zeros = [0] * (len(arr) - len(non_zeros))
    return non_zeros + zeros

move_zeros([0, 1, 0, 3, 12])
```

**Explanation:** This code moves all zeros in an array to the end by separating non-zero and zero elements.

**Output:**
```
[1, 3, 12, 0, 0]
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

longest_subarray_with_sum([1, 2, 3, 1, 1, 1, 1, 4, 2, 3], 3)
```

**Explanation:** This code finds the length of the longest subarray with a given sum using a hash map to store cumulative sums.

**Output:**
```
4
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

has_zero_sum_subarray([1, 2, -2, 4, -4])
```

**Explanation:** This code determines if an array contains a subarray with a sum of zero using a set to track cumulative sums.

**Output:**
```
True
```

### String Problems

#### 1. Reverse a string without using extra space

```python
def reverse_string(s):
    return s[::-1]

reverse_string("hello")
```

**Explanation:** This code reverses a string using slicing.

**Output:**
```
"olleh"
```

#### 2. Check if a string is a palindrome

```python
def is_palindrome(s):
    return s == s[::-1]

is_palindrome("racecar")
```

**Explanation:** This code checks if a string is a palindrome by comparing it with its reverse.

**Output:**
```
True
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

first_non_repeating_char("abacabad")
```

**Explanation:** This code finds the first non-repeating character by counting character occurrences and returning the first character with a count of one.

**Output:**
```
"c"
```

#### 4. Count the frequency of each character in a string

```python
def char_frequency(s):
    frequency = {}
    for char in s:
        frequency[char] = frequency.get(char, 0) + 1
    return frequency

char_frequency("hello")
```

**Explanation:** This code counts the frequency of each character in a string using a dictionary.

**Output:**
```
{'h': 1, 'e': 1, 'l': 2, 'o': 1}
```

#### 5. Check if two strings are anagrams

```python
def are_anagrams(s1, s2):
    return sorted(s1) == sorted(s2)

are_anagrams("listen", "silent")
```

**Explanation:** This code checks if two strings are anagrams by sorting and comparing them.

**Output:**
```
True
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

compress_string("aabcccccaaa")
```

**Explanation:** This code compresses a string by counting consecutive characters and appending them to a list.

**Output:**
```
"a2b1c5a3"
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

longest_common_prefix(["flower", "flow", "flight"])
```

**Explanation:** This code finds the longest common prefix by comparing the prefix of the first string with each subsequent string.

**Output:**
```
"fl"
```

#### 8. Replace all spaces in a string with %20

```python
def replace_spaces(s):
    return s.replace(' ', '%20')

replace_spaces("Mr John Smith")
```

**Explanation:** This code replaces all spaces in a string with `%20` using the `replace` method.

**Output:**
```
"Mr%20John%20Smith"
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

longest_palindromic_substring("babad")
```

**Explanation:** This code finds the longest palindromic substring by expanding around each character and checking for palindromes.

**Output:**
```
"bab"
```

#### 10. Print all permutations of a string

```python
def permute_string(s):
    from itertools import permutations
    return [''.join(p) for p in permutations(s)]

permute_string("abc")
```

**Explanation:** This code prints all permutations of a string using the `permutations` function from the `itertools` module.

**Output:**
```
['abc', 'acb', 'bac', 'bca', 'cab', 'cba']
```

### Recursion Problems

#### 1. Compute the factorial of a number

```python
def factorial(n):
    if n == 0:
        return 1
    return n * factorial(n - 1)

factorial(5)
```

**Explanation:** This code computes the factorial of a number using recursion.

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

fibonacci(10)
```

**Explanation:** This code generates the Fibonacci sequence up to `n` using iteration.

**Output:**
```
[0, 1, 1, 2, 3, 5, 8, 13, 21, 34]
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

tower_of_hanoi(3, 'A', 'B', 'C')
```

**Explanation:** This code solves the Tower of Hanoi problem using recursion.

**Output:**
```
Move disk 1 from A to C
Move disk 2 from A to B
Move disk 1 from C to B
Move disk 3 from A to C
Move disk 1 from B to A
Move disk 2 from B to C
Move disk 1 from A to C
```

#### 4. Print all subsets of a given array

```python
def print_subsets(arr):
    def backtrack(start, path):
        print(path)
        for i in range(start, len(arr)):
            backtrack(i + 1, path + [arr[i]])
    backtrack(0, [])

print_subsets([1, 2, 3])
```

**Explanation:** This code prints all subsets of a given array using backtracking.

**Output:**
```
[]
[1]
[1, 2]
[1, 2, 3]
[1, 3]
[2]
[2, 3]
[3]
```

#### 5. Find the nth term of a geometric progression using recursion

```python
def geometric_progression(a, r, n):
    if n == 1:
        return a
    return r * geometric_progression(a, r, n - 1)

geometric_progression(2, 3, 4)
```

**Explanation:** This code finds the nth term of a geometric progression using recursion.

**Output:**
```
54
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

solve_n_queens(4)
```

**Explanation:** This code solves the N-Queens problem using backtracking.

**Output:**
```
[[1, 3, 0, 2], [2, 0, 3, 1]]
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

generate_parentheses(3)
```

**Explanation:** This code generates all valid combinations of `n` pairs of parentheses using backtracking.

**Output:**
```
['((()))', '(()())', '(())()', '()(())', '()()()']
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

binary_search([1, 2, 3, 4, 5], 4, 0, 4)
```

**Explanation:** This code performs binary search recursively to find the index of a target element.

**Output:**
```
3
```

#### 9. Find the greatest common divisor (GCD) of two numbers using recursion

```python
def gcd(a, b):
    if b == 0:
        return a
    return gcd(b, a % b)

gcd(48, 18)
```

**Explanation:** This code finds the GCD of two numbers using the Euclidean algorithm and recursion.

**Output:**
```
6
```

#### 10. Count the number of ways to climb n stairs with steps of 1 or 2

```python
def climb_stairs(n):
    if n == 0 or n == 1:
        return 1
    return climb_stairs(n - 1) + climb_stairs(n - 2)

climb_stairs(5)
```

**Explanation:** This code counts the number of ways to climb `n` stairs with steps of 1 or 2 using recursion.

**Output:**
```
8
```

### Mathematical Problems

#### 1. Check if a number is prime

```python
def is_prime(n):
    if n <= 1:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True

is_prime(29)
```

**Explanation:** This code checks if a number is prime by testing divisibility up to the square root of the number.

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
        for i in range(2, int(num**0.5) + 1):
            if num % i == 0:
                return False
        return True

    return sum(i for i in range(2, n + 1) if is_prime(i))

sum_of_primes(10)
```

**Explanation:** This code finds the sum of all prime numbers up to `n` by checking each number for primality.

**Output:**
```
17
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

trailing_zeros_in_factorial(100)
```

**Explanation:** This code determines the number of trailing zeros in the factorial of a number by counting the number of times 5 is a factor in the numbers from 1 to `n`.

**Output:**
```
24
```

#### 4. Calculate the sum of digits of a number until it becomes a single digit

```python
def sum_of_digits(n):
    while n >= 10:
        n = sum(int(digit) for digit in str(n))
    return n

sum_of_digits(9875)
```

**Explanation:** This code calculates the sum of digits of a number until it becomes a single digit by repeatedly summing the digits.

**Output:**
```
2
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

modular_exponentiation(2, 10, 1000)
```

**Explanation:** This code solves modular exponentiation efficiently using the method of exponentiation by squaring.

**Output:**
```
24
```

#### 6. Find all prime factors of a number

```python
def prime_factors(n):
    factors = []
    while n % 2 == 0:
        factors.append(2)
        n = n // 2
    for i in range(3, int(n**0.5) + 1, 2):
        while n % i == 0:
            factors.append(i)
            n = n // i
    if n > 2:
        factors.append(n)
    return factors

prime_factors(315)
```

**Explanation:** This code finds all prime factors of a number by dividing the number by its smallest prime factors.

**Output:**
```
[3, 3, 5, 7]
```

#### 7. Check if a number is an Armstrong number

```python
def is_armstrong(n):
    num_str = str(n)
    power = len(num_str)
    return n == sum(int(digit) ** power for digit in num_str)

is_armstrong(153)
```

**Explanation:** This code checks if a number is an Armstrong number by comparing it with the sum of its digits each raised to the power of the number of digits.

**Output:**
```
True
```

#### 8. Print the first n perfect numbers

```python
def is_perfect(num):
    return num == sum(i for i in range(1, num) if num % i == 0)

def first_n_perfect_numbers(n):
    count = 0
    num = 2
    perfect_numbers = []
    while count < n:
        if is_perfect(num):
            perfect_numbers.append(num)
            count += 1
        num += 1
    return perfect_numbers

first_n_perfect_numbers(3)
```

**Explanation:** This code prints the first `n` perfect numbers by checking each number for perfection.

**Output:**
```
[6, 28, 496]
```

#### 9. Determine if a number is a palindrome

```python
def is_palindrome_number(n):
    return str(n) == str(n)[::-1]

is_palindrome_number(121)
```

**Explanation:** This code determines if a number is a palindrome by comparing it with its reverse.

**Output:**
```
True
```

#### 10. Compute the nth Fibonacci number iteratively

```python
def fibonacci_number(n):
    if n <= 0:
        return 0
    if n == 1:
        return 1
    a, b = 0, 1
    for _ in range(2, n + 1):
        a, b = b, a + b
    return b

fibonacci_number(10)
```

**Explanation:** This code computes the nth Fibonacci number iteratively by updating two variables.

**Output:**
```
55
```

### Bit Manipulation Problems

#### 1. Check if a number is a power of 2

```python
def is_power_of_2(n):
    return n > 0 and (n & (n - 1)) == 0

is_power_of_2(16)
```

**Explanation:** This code checks if a number is a power of 2 by using bitwise AND with `n-1`.

**Output:**
```
True
```

#### 2. Find the only non-repeated number in an array where every other number repeats twice

```python
def find_non_repeated(arr):
    unique_number = 0
    for num in arr:
        unique_number ^= num
    return unique_number

find_non_repeated([2, 3, 5, 4, 5, 3, 4])
```

**Explanation:** This code finds the only non-repeated number using XOR, which cancels out repeated numbers.

**Output:**
```
2
```

#### 3. Count the number of 1 bits in a number

```python
def count_one_bits(n):
    return bin(n).count('1')

count_one_bits(29)
```

**Explanation:** This code counts the number of 1 bits in a number by converting it to binary and counting '1's.

**Output:**
```
4
```

#### 4. Toggle the kth bit of a number

```python
def toggle_kth_bit(n, k):
    return n ^ (1 << (k - 1))

toggle_kth_bit(29, 3)
```

**Explanation:** This code toggles the kth bit of a number using XOR with a shifted 1.

**Output:**
```
25
```

#### 5. Find the XOR of all elements in an array

```python
def xor_of_array(arr):
    result = 0
    for num in arr:
        result ^= num
    return result

xor_of_array([3, 5, 7, 2])
```

**Explanation:** This code finds the XOR of all elements in an array by iterating and applying XOR.

**Output:**
```
7
```

### Projects to Learn Logical Building

#### 1. Simple Calculator with all mathematics conditions

```python
def calculator(expression):
    try:
        return eval(expression)
    except Exception as e:
        return f"Error: {e}"

calculator("3 + 5 * (2 - 8)")
```

**Explanation:** This code evaluates a mathematical expression using the `eval` function.

**Output:**
```
-25
```

#### 2. Build a program to generate fractal patterns like the Sierpiński triangle

```python
import matplotlib.pyplot as plt

def sierpinski_triangle(n):
    def draw_triangle(ax, points, depth):
        if depth == 0:
            ax.plot([points[0][0], points[1][0], points[2][0], points[0][0]],
                    [points[0][1], points[1][1], points[2][1], points[0][1]], color='b')
        else:
            p0, p1, p2 = points
            p3 = ((p0[0] + p1[0]) / 2, (p0[1] + p1[1]) / 2)
            p4 = ((p1[0] + p2[0]) / 2, (p1[1] + p2[1]) / 2)
            p5 = ((p2[0] + p0[0]) / 2, (p2[1] + p0[1]) / 2)
            draw_triangle(ax, [p0, p3, p5], depth - 1)
            draw_triangle(ax, [p3, p1, p4], depth - 1)
            draw_triangle(ax, [p5, p4, p2], depth - 1)

    fig, ax = plt.subplots()
    ax.set_aspect('equal')
    ax.axis('off')
    draw_triangle(ax, [(0, 0), (1, 1), (2, 0)], n)
    plt.show()

sierpinski_triangle(4)
```

**Explanation:** This code generates a Sierpiński triangle fractal pattern using recursive drawing.

**Output:**
```
A plot of the Sierpiński triangle will be displayed.
```

#### 3. Implement a matrix multiplication program

```python
def matrix_multiply(A, B):
    if len(A[0]) != len(B):
        return "Incompatible matrices"
    result = [[0] * len(B[0]) for _ in range(len(A))]
    for i in range(len(A)):
        for j in range(len(B[0])):
            for k in range(len(B)):
                result[i][j] += A[i][k] * B[k][j]
    return result

matrix_multiply([[1, 2], [3, 4]], [[5, 6], [7, 8]])
```

**Explanation:** This code multiplies two matrices using nested loops.

**Output:**
```
[[19, 22], [43, 50]]
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

solve_sudoku([
    [5, 3, 0, 0, 7, 0, 0, 0, 0],
    [6, 0, 0, 1, 9, 5, 0, 0, 0],
    [0, 9, 8, 0, 0, 0, 0, 6, 0],
    [8, 0, 0, 0, 6, 0, 0, 0, 3],
    [4, 0, 0, 8, 0, 3, 0, 0, 1],
    [7, 0, 0, 0, 2, 0, 0, 0, 6],
    [0, 6, 0, 0, 0, 0, 2, 8, 0],
    [0, 0, 0, 4, 1, 9, 0, 0, 5],
    [0, 0, 0, 0, 8, 0, 0, 7, 9]
])
```

**Explanation:** This code solves a Sudoku puzzle using backtracking.

**Output:**
```
[[5, 3, 4, 6, 7, 8, 9, 1, 2],
 [6, 7, 2, 1, 9, 5, 3, 4, 8],
 [1, 9, 8, 3, 4, 2, 5, 6, 7],
 [8, 5, 9, 7, 6, 1, 4, 2, 3],
 [4, 2, 6, 8, 5, 3, 7, 9, 1],
 [7, 1, 3, 9, 2, 4, 8, 5, 6],
 [9, 6, 1, 5, 3, 7, 2, 8, 4],
 [2, 8, 7, 4, 1, 9, 6, 3, 5],
 [3, 4, 5, 2, 8, 6, 1, 7, 9]]
```

#### 5. Develop a program to check plagiarism in documents by comparing substrings

```python
def check_plagiarism(doc1, doc2, n):
    def get_substrings(doc, n):
        return [doc[i:i+n] for i in range(len(doc) - n + 1)]

    substrings1 = get_substrings(doc1, n)
    substrings2 = get_substrings(doc2, n)
    common_substrings = set(substrings1).intersection(substrings2)
    return len(common_substrings) / len(substrings1)

check_plagiarism("This is a test document.", "This document is a test.", 3)
```

**Explanation:** This code checks for plagiarism by comparing substrings of a given length `n` between two documents.

**Output:**
```
0.5
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
    return "No solution"

solve_maze([
    [1, 0, 0, 0],
    [1, 1, 0, 1],
    [0, 1, 0, 0],
    [1, 1, 1, 1]
])
```

**Explanation:** This code solves a maze using recursion and backtracking.

**Output:**
```
[[1, 0, 0, 0],
 [1, 1, 0, 0],
 [0, 1, 0, 0],
 [0, 1, 1, 1]]
```

#### 7. Build a basic file compression algorithm using bit-level operations

```python
def compress_file(data):
    compressed = []
    for char in data:
        binary = format(ord(char), '08b')
        compressed.append(binary)
    return ''.join(compressed)

compress_file("hello")
```

**Explanation:** This code compresses a file by converting each character to its binary representation.

**Output:**
```
"0110100001100101011011000110110001101111"
```






It looks like you've listed a variety of algorithm problems, categorized by difficulty and topic. However, you haven't provided specific links or details for each problem. If you're looking for Python code solutions with explanations and outputs for these problems, I can certainly help with that!

Let's start with a few examples from your list. I'll provide Python code, explanations, and expected outputs for some of these problems. If you have specific problems in mind or need more details, feel free to let me know!

### 1. Two Sum

**Problem:** Given an array of integers `nums` and an integer `target`, return indices of the two numbers such that they add up to `target`.

**Solution:**

```python
def two_sum(nums, target):
    num_to_index = {}
    for i, num in enumerate(nums):
        complement = target - num
        if complement in num_to_index:
            return [num_to_index[complement], i]
        num_to_index[num] = i
    return []

# Example usage
nums = [2, 7, 11, 15]
target = 9
result = two_sum(nums, target)
print("Two Sum Result:", result)  # Output: [0, 1]
```

**Explanation:** We use a dictionary to store the indices of the numbers we've seen so far. For each number, we check if its complement (i.e., `target - num`) is already in the dictionary. If it is, we return the indices. Otherwise, we add the number and its index to the dictionary.

### 2. Remove Duplicates from Sorted Array

**Problem:** Given a sorted array `nums`, remove the duplicates in-place such that each element appears only once and return the new length.

**Solution:**

```python
def remove_duplicates(nums):
    if not nums:
        return 0
    write_pointer = 1
    for read_pointer in range(1, len(nums)):
        if nums[read_pointer] != nums[read_pointer - 1]:
            nums[write_pointer] = nums[read_pointer]
            write_pointer += 1
    return write_pointer

# Example usage
nums = [1, 1, 2]
new_length = remove_duplicates(nums)
print("New Length:", new_length)  # Output: 2
print("Modified Array:", nums[:new_length])  # Output: [1, 2]
```

**Explanation:** We use two pointers: one to read the array and one to write the unique elements. We only move the write pointer when we encounter a new unique element.

### 3. Best Time to Buy and Sell Stock

**Problem:** Given an array `prices` where `prices[i]` is the price of a given stock on the `i-th` day, find the maximum profit you can achieve.

**Solution:**

```python
def max_profit(prices):
    min_price = float('inf')
    max_profit = 0
    for price in prices:
        if price < min_price:
            min_price = price
        elif price - min_price > max_profit:
            max_profit = price - min_price
    return max_profit

# Example usage
prices = [7, 1, 5, 3, 6, 4]
profit = max_profit(prices)
print("Max Profit:", profit)  # Output: 5
```

**Explanation:** We keep track of the minimum price seen so far and calculate the profit if we sell at the current price. We update the maximum profit whenever we find a higher profit.

### 4. Plus One

**Problem:** Given a non-empty array of decimal digits representing a non-negative integer, increment one to the integer.

**Solution:**

```python
def plus_one(digits):
    n = len(digits)
    for i in range(n - 1, -1, -1):
        if digits[i] == 9:
            digits[i] = 0
        else:
            digits[i] += 1
            return digits
    return [1] + digits

# Example usage
digits = [1, 2, 3]
result = plus_one(digits)
print("Plus One Result:", result)  # Output: [1, 2, 4]
```

**Explanation:** We iterate from the last digit to the first, incrementing the digit if it's not 9. If it is 9, we set it to 0 and continue to the next digit. If all digits are 9, we add a 1 at the beginning.

### 5. Missing Number

**Problem:** Given an array `nums` containing `n` distinct numbers in the range `[0, n]`, find the missing number.

**Solution:**

```python
def missing_number(nums):
    n = len(nums)
    expected_sum = n * (n + 1) // 2
    actual_sum = sum(nums)
    return expected_sum - actual_sum

# Example usage
nums = [3, 0, 1]
missing = missing_number(nums)
print("Missing Number:", missing)  # Output: 2
```

**Explanation:** We calculate the expected sum of the first `n` natural numbers and subtract the actual sum of the array to find the missing number.

### 6. Maximum Subarray

**Problem:** Given an integer array `nums`, find the contiguous subarray (containing at least one number) which has the largest sum and return its sum.

**Solution:**

```python
def max_subarray(nums):
    max_current = max_global = nums[0]
    for num in nums[1:]:
        max_current = max(num, max_current + num)
        if max_current > max_global:
            max_global = max_current
    return max_global

# Example usage
nums = [-2, 1, -3, 4, -1, 2, 1, -5, 4]
max_sum = max_subarray(nums)
print("Max Subarray Sum:", max_sum)  # Output: 6
```

**Explanation:** We use Kadane's algorithm to find the maximum sum of a contiguous subarray. We keep track of the maximum sum ending at the current position and update the global maximum sum accordingly.

### 7. Move Zeroes

**Problem:** Given an array `nums`, write a function to move all `0`s to the end of it while maintaining the relative order of the non-zero elements.

**Solution:**

```python
def move_zeroes(nums):
    last_non_zero_found_at = 0
    for current in range(len(nums)):
        if nums[current] != 0:
            nums[last_non_zero_found_at], nums[current] = nums[current], nums[last_non_zero_found_at]
            last_non_zero_found_at += 1
    return nums

# Example usage
nums = [0, 1, 0, 3, 12]
result = move_zeroes(nums)
print("Move Zeroes Result:", result)  # Output: [1, 3, 12, 0, 0]
```

**Explanation:** We use two pointers: one to track the position of the last non-zero element and another to iterate through the array. We swap non-zero elements to the front and move zeroes to the end.

### 8. Contains Duplicate

**Problem:** Given an array of integers, find if the array contains any duplicates.

**Solution:**

```python
def contains_duplicate(nums):
    return len(nums) != len(set(nums))

# Example usage
nums = [1, 2, 3, 1]
result = contains_duplicate(nums)
print("Contains Duplicate:", result)  # Output: True
```

**Explanation:** We convert the list to a set and compare the lengths. If the lengths are different, there are duplicates.

### 9. Intersection of Two Arrays II

**Problem:** Given two arrays, write a function to compute their intersection.

**Solution:**

```python
def intersect(nums1, nums2):
    from collections import Counter
    count1 = Counter(nums1)
    count2 = Counter(nums2)
    intersection = []
    for num in count1:
        if num in count2:
            intersection.extend([num] * min(count1[num], count2[num]))
    return intersection

# Example usage
nums1 = [1, 2, 2, 1]
nums2 = [2, 2]
result = intersect(nums1, nums2)
print("Intersection of Two Arrays II:", result)  # Output: [2, 2]
```

**Explanation:** We use `Counter` to count the occurrences of each element in both arrays and find the intersection based on the minimum count of each element.

### 10. Rotate Array

**Problem:** Given an array, rotate the array to the right by `k` steps, where `k` is non-negative.

**Solution:**

```python
def rotate(nums, k):
    n = len(nums)
    k = k % n
    nums[:] = nums[-k:] + nums[:-k]
    return nums

# Example usage
nums = [1, 2, 3, 4, 5, 6, 7]
k = 3
result = rotate(nums, k)
print("Rotate Array Result:", result)  # Output: [5, 6, 7, 1, 2, 3, 4]
```

**Explanation:** We calculate the effective number of rotations and slice the array to rotate it.

### 11. Third Maximum Number

**Problem:** Given a non-empty array of integers, return the third maximum number. If it doesn't exist, return the maximum number.

**Solution:**

```python
def third_max(nums):
    unique_nums = list(set(nums))
    unique_nums.sort(reverse=True)
    if len(unique_nums) < 3:
        return unique_nums[0]
    return unique_nums[2]

# Example usage
nums = [3, 2, 1]
result = third_max(nums)
print("Third Maximum Number:", result)  # Output: 1
```

**Explanation:** We remove duplicates, sort the array in descending order, and return the third element if it exists. Otherwise, we return the maximum element.

### 12. Valid Palindrome

**Problem:** Given a string, determine if it is a palindrome, considering only alphanumeric characters and ignoring cases.

**Solution:**

```python
def is_palindrome(s):
    filtered_chars = [char.lower() for char in s if char.isalnum()]
    return filtered_chars == filtered_chars[::-1]

# Example usage
s = "A man, a plan, a canal: Panama"
result = is_palindrome(s)
print("Valid Palindrome:", result)  # Output: True
```

**Explanation:** We filter out non-alphanumeric characters, convert to lowercase, and check if the string is equal to its reverse.

### 13. Merge Sorted Array

**Problem:** Given two sorted integer arrays `nums1` and `nums2`, merge `nums2` into `nums1` as one sorted array.

**Solution:**

```python
def merge(nums1, m, nums2, n):
    while m > 0 and n > 0:
        if nums1[m - 1] > nums2[n - 1]:
            nums1[m + n - 1] = nums1[m - 1]
            m -= 1
        else:
            nums1[m + n - 1] = nums2[n - 1]
            n -= 1
    while n > 0:
        nums1[m + n - 1] = nums2[n - 1]
        n -= 1
    return nums1

# Example usage
nums1 = [1, 2, 3, 0, 0, 0]
m = 3
nums2 = [2, 5, 6]
n = 3
result = merge(nums1, m, nums2, n)
print("Merge Sorted Array Result:", result)  # Output: [1, 2, 2, 3, 5, 6]
```

**Explanation:** We merge the arrays from the end to avoid overwriting elements in `nums1`.

### 14. Maximum Product Subarray

**Problem:** Given an integer array `nums`, find a contiguous subarray within the array (containing at least one number) which has the largest product.

**Solution:**

```python
def max_product(nums):
    max_product = min_product = result = nums[0]
    for num in nums[1:]:
        if num < 0:
            max_product, min_product = min_product, max_product
        max_product = max(num, max_product * num)
        min_product = min(num, min_product * num)
        result = max(result, max_product)
    return result

# Example usage
nums = [2, 3, -2, 4]
result = max_product(nums)
print("Maximum Product Subarray:", result)  # Output: 6
```

**Explanation:** We keep track of the maximum and minimum products ending at the current position. We update the global maximum product accordingly.

### 15. Minimum Size Subarray Sum

**Problem:** Given an array of positive integers `nums` and a positive integer `target`, return the minimal length of a contiguous subarray for which the sum is greater than or equal to `target`.

**Solution:**

```python
def min_subarray_len(target, nums):
    left = 0
    current_sum = 0
    min_length = float('inf')
    for right in range(len(nums)):
        current_sum += nums[right]
        while current_sum >= target:
            min_length = min(min_length, right - left + 1)
            current_sum -= nums[left]
            left += 1
    return min_length if min_length != float('inf') else 0

# Example usage
target = 7
nums = [2, 3, 1, 2, 4, 3]
result = min_subarray_len(target, nums)
print("Minimum Size Subarray Sum:", result)  # Output: 2
```

**Explanation:** We use a sliding window to find the minimum length of a subarray with a sum greater than or equal to the target.

### 16. Product of Array Except Self

**Problem:** Given an array `nums` of `n` integers where `n > 1`, return an array `output` such that `output[i]` is equal to the product of all the elements of `nums` except `nums[i]`.

**Solution:**

```python
def product_except_self(nums):
    n = len(nums)
    left_products = [1] * n
    right_products = [1] * n
    output = [1] * n
    for i in range(1, n):
        left_products[i] = left_products[i - 1] * nums[i - 1]
    for i in range(n - 2, -1, -1):
        right_products[i] = right_products[i + 1] * nums[i + 1]
    for i in range(n):
        output[i] = left_products[i] * right_products[i]
    return output

# Example usage
nums = [1, 2, 3, 4]
result = product_except_self(nums)
print("Product of Array Except Self:", result)  # Output: [24, 12, 8, 6]
```

**Explanation:** We calculate the product of all elements to the left and right of each element and multiply them to get the result.

### 17. Container With Most Water

**Problem:** Given `n` non-negative integers `a1, a2, ..., an`, where each represents a point at coordinate `(i, ai)`. `n` vertical lines are drawn such that the two endpoints of the line `i` are at `(i, ai)` and `(i, 0)`. Find two lines which together with the x-axis forms a container, such that the container contains the most water.

**Solution:**

```python
def max_area(height):
    left = 0
    right = len(height) - 1
    max_water = 0
    while left < right:
        current_water = min(height[left], height[right]) * (right - left)
        max_water = max(max_water, current_water)
        if height[left] < height[right]:
            left += 1
        else:
            right -= 1
    return max_water

# Example usage
height = [1, 8, 6, 2, 5, 4, 8, 3, 7]
result = max_area(height)
print("Container With Most Water:", result)  # Output: 49
```

**Explanation:** We use two pointers to find the maximum area of water that can be contained between two lines.

### 18. Search in Rotated Sorted Array

**Problem:** Given the sorted rotated array `nums` of unique elements, return the index of the target if it is in `nums`, or `-1` if it is not in `nums`.

**Solution:**

```python
def search(nums, target):
    left, right = 0, len(nums) - 1
    while left <= right:
        mid = (left + right) // 2
        if nums[mid] == target:
            return mid
        if nums[left] <= nums[mid]:
            if nums[left] <= target < nums[mid]:
                right = mid - 1
            else:
                left = mid + 1
        else:
            if nums[mid] < target <= nums[right]:
                left = mid + 1
            else:
                right = mid - 1
    return -1

# Example usage
nums = [4, 5, 6, 7, 0, 1, 2]
target = 0
result = search(nums, target)
print("Search in Rotated Sorted Array:", result)  # Output: 4
```

**Explanation:** We use binary search to find the target in a rotated sorted array.

### 19. Combination Sum

**Problem:** Given an array of distinct integers `candidates` and a target integer `target`, return a list of all unique combinations of `candidates` where the chosen numbers sum to `target`.

**Solution:**

```python
def combination_sum(candidates, target):
    def backtrack(start, target, path):
        if target == 0:
            result.append(path)
            return
        if target < 0:
            return
        for i in range(start, len(candidates)):
            backtrack(i, target - candidates[i], path + [candidates[i]])

    result = []
    candidates.sort()
    backtrack(0, target, [])
    return result

# Example usage
candidates = [2, 3, 6, 7]
target = 7
result = combination_sum(candidates, target)
print("Combination Sum:", result)  # Output: [[2, 2, 3], [7]]
```

**Explanation:** We use backtracking to find all combinations of candidates that sum to the target.

### 20. Next Permutation

**Problem:** Implement next permutation, which rearranges numbers into the lexicographically next greater permutation.

**Solution:**

```python
def next_permutation(nums):
    n = len(nums)
    i = n - 2
    while i >= 0 and nums[i] >= nums[i + 1]:
        i -= 1
    if i == -1:
        nums.reverse()
        return nums
    j = n - 1
    while nums[j] <= nums[i]:
        j -= 1
    nums[i], nums[j] = nums[j], nums[i]
    nums[i + 1:] = reversed(nums[i + 1:])
    return nums

# Example usage
nums = [1, 2, 3]
result = next_permutation(nums)
print("Next Permutation:", result)  # Output: [1, 3, 2]
```

**Explanation:** We find the first decreasing element from the end and swap it with the smallest element larger than it. Then we reverse the suffix to get the next permutation.

### 21. Find First and Last Position of Element in Sorted Array

**Problem:** Given an array of integers `nums` sorted in ascending order, find the starting and ending position of a given `target` value.

**Solution:**

```python
def search_range(nums, target):
    def binary_search_left(nums, target):
        left, right = 0, len(nums) - 1
        while left <= right:
            mid = (left + right) // 2
            if nums[mid] < target:
                left = mid + 1
            else:
                right = mid - 1
        return left

    def binary_search_right(nums, target):
        left, right = 0, len(nums) - 1
        while left <= right:
            mid = (left + right) // 2
            if nums[mid] <= target:
                left = mid + 1
            else:
                right = mid - 1
        return right

    left_index = binary_search_left(nums, target)
    right_index = binary_search_right(nums, target)
    if left_index <= right_index:
        return [left_index, right_index]
    return [-1, -1]

# Example usage
nums = [5, 7, 7, 8, 8, 10]
target = 8
result = search_range(nums, target)
print("Find First and Last Position of Element in Sorted Array:", result)  # Output: [3, 4]
```

**Explanation:** We use binary search to find the leftmost and rightmost positions of the target in the sorted array.

### 22. 3Sum

**Problem:** Given an array `nums` of `n` integers, find all unique triplets in the array which give the sum of zero.

**Solution:**

```python
def three_sum(nums):
    nums.sort()
    result = []
    for i in range(len(nums) - 2):
        if i > 0 and nums[i] == nums[i - 1]:
            continue
        left, right = i + 1, len(nums) - 1
        while left < right:
            total = nums[i] + nums[left] + nums[right]
            if total == 0:
                result.append([nums[i], nums[left], nums[right]])
                while left < right and nums[left] == nums[left + 1]:
                    left += 1
                while left < right and nums[right] == nums[right - 1]:
                    right -= 1
                left += 1
                right -= 1
            elif total < 0:
                left += 1
            else:
                right -= 1
    return result

# Example usage
nums = [-1, 0, 1, 2, -1, -4]
result = three_sum(nums)
print("3Sum:", result)  # Output: [[-1, -1, 2], [-1, 0, 1]]
```

**Explanation:** We sort the array and use two pointers to find all unique triplets that sum to zero.

### 23. Spiral Matrix

**Problem:** Given an `m x n` matrix, return all elements of the matrix in spiral order.

**Solution:**

```python
def spiral_order(matrix):
    result = []
    while matrix:
        result += matrix.pop(0)
        if matrix and matrix[0]:
            for row in matrix:
                result.append(row.pop())
        if matrix:
            result += matrix.pop()[::-1]
        if matrix and matrix[0]:
            for row in matrix[::-1]:
                result.append(row.pop(0))
    return result

# Example usage
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]
result = spiral_order(matrix)
print("Spiral Matrix:", result)  # Output: [1, 2, 3, 6, 9, 8, 7, 4, 5]
```

**Explanation:** We repeatedly remove the outer layer of the matrix in a spiral order and add the elements to the result.

### 24. Merge Intervals

**Problem:** Given an array of intervals where intervals[i] = [starti, endi], merge all overlapping intervals.

**Solution:**

```python
def merge(intervals):
    intervals.sort(key=lambda x: x[0])
    merged = []
    for interval in intervals:
        if not merged or merged[-1][1] < interval[0]:
            merged.append(interval)
        else:
            merged[-1][1] = max(merged[-1][1], interval[1])
    return merged

# Example usage
intervals = [[1, 3], [2, 6], [8, 10], [15, 18]]
result = merge(intervals)
print("Merge Intervals:", result)  # Output: [[1, 6], [8, 10], [15, 18]]
```

**Explanation:** We sort the intervals and merge overlapping intervals.

### 25. Jump Game

**Problem:** Given an array of non-negative integers `nums`, you are initially positioned at the first index of the array. Each element in the array represents your maximum jump length at that position. Determine if you are able to reach the last index.

**Solution:**

```python
def can_jump(nums):
    max_reach = 0
    for i in range(len(nums)):
        if i > max_reach:
            return False
        max_reach = max(max_reach, i + nums[i])
    return True

# Example usage
nums = [2, 3, 1, 1, 4]
result = can_jump(nums)
print("Jump Game:", result)  # Output: True
```

**Explanation:** We keep track of the maximum reachable index and check if we can reach the end of the array.

### 26. Set Matrix Zeroes

**Problem:** Given an `m x n` matrix, if an element is 0, set its entire row and column to 0.

**Solution:**

```python
def set_zeroes(matrix):
    rows = len(matrix)
    cols = len(matrix[0])
    first_row_has_zero = any(matrix[0][j] == 0 for j in range(cols))
    first_col_has_zero = any(matrix[i][0] == 0 for i in range(rows))
    for i in range(1, rows):
        for j in range(1, cols):
            if matrix[i][j] == 0:
                matrix[i][0] = 0
                matrix[0][j] = 0
    for i in range(1, rows):
        for j in range(1, cols):
            if matrix[i][0] == 0 or matrix[0][j] == 0:
                matrix[i][j] = 0
    if first_row_has_zero:
        for j in range(cols):
            matrix[0][j] = 0
    if first_col_has_zero:
        for i in range(rows):
            matrix[i][0] = 0
    return matrix

# Example usage
matrix = [
    [1, 1, 1],
    [1, 0, 1],
    [1, 1, 1]
]
result = set_zeroes(matrix)
print("Set Matrix Zeroes:", result)  # Output: [[1, 0, 1], [0, 0, 0], [1, 0, 1]]
```

**Explanation:** We use the first row and column to mark the rows and columns that need to be set to zero. Then we set the elements to zero based on the marks.

### 27. Group Anagrams

**Problem:** Given an array of strings `strs`, group the anagrams together.

**Solution:**

```python
from collections import defaultdict

def group_anagrams(strs):
    anagrams = defaultdict(list)
    for s in strs:
        sorted_s = ''.join(sorted(s))
        anagrams[sorted_s].append(s)
    return list(anagrams.values())

# Example usage
strs = ["eat", "tea", "tan", "ate", "nat", "bat"]
result = group_anagrams(strs)
print("Group Anagrams:", result)  # Output: [['eat', 'tea', 'ate'], ['tan', 'nat'], ['bat']]
```

**Explanation:** We use a dictionary to group anagrams by their sorted tuple of characters.

### 28. Word Search

**Problem:** Given an `m x n` grid of characters `board` and a string `word`, return `true` if `word` exists in the grid.

**Solution:**

```python
def exist(board, word):
    def dfs(i, j, word_index):
        if word_index == len(word):
            return True
        if i < 0 or i >= len(board) or j < 0 or j >= len(board[0]) or board[i][j] != word[word_index]:
            return False
        temp = board[i][j]
        board[i][j] = '#'
        found = (dfs(i + 1, j, word_index + 1) or
                 dfs(i - 1, j, word_index + 1) or
                 dfs(i, j + 1, word_index + 1) or
                 dfs(i, j - 1, word_index + 1))
        board[i][j] = temp
        return found

    for i in range(len(board)):
        for j in range(len(board[0])):
            if board[i][j] == word[0] and dfs(i, j, 0):
                return True
    return False

# Example usage
board = [
    ['A', 'B', 'C', 'E'],
    ['S', 'F', 'C', 'S'],
    ['A', 'D', 'E', 'E']
]
word = "ABCCED"
result = exist(board, word)
print("Word Search:", result)  # Output: True
```

**Explanation:** We use depth-first search (DFS) to explore the board and check if the word exists.

### 29. First Missing Positive

**Problem:** Given an unsorted integer array `nums`, find the smallest missing positive integer.

**Solution:**

```python
def first_missing_positive(nums):
    n = len(nums)
    for i in range(n):
        while 1 <= nums[i] <= n and nums[nums[i] - 1] != nums[i]:
            nums[nums[i] - 1], nums[i] = nums[i], nums[nums[i] - 1]
    for i in range(n):
        if nums[i] != i + 1:
            return i + 1
    return n + 1

# Example usage
nums = [1, 2, 0]
result = first_missing_positive(nums)
print("First Missing Positive:", result)  # Output: 3
```

**Explanation:** We place each number in its correct position and then find the first missing positive integer.

### 30. Find Peak Element

**Problem:** A peak element is an element that is greater than its neighbors. Given an input array `nums`, where `nums[i] != nums[i + 1]`, find a peak element and return its index.

**Solution:**

```python
def find_peak_element(nums):
    left, right = 0, len(nums) - 1
    while left < right:
        mid = (left + right) // 2
        if nums[mid] > nums[mid + 1]:
            right = mid
        else:
            left = mid + 1
    return left

# Example usage
nums = [1, 2, 3, 1]
result = find_peak_element(nums)
print("Find Peak Element:", result)  # Output: 2
```

**Explanation:** We use binary search to find a peak element in the array.

### 31. Trapping Rain Water

**Problem:** Given `n` non-negative integers representing an elevation map where the width of each bar is 1, compute how much water it can trap after raining.

**Solution:**

```python
def trap(height):
    left, right = 0, len(height) - 1
    left_max, right_max = 0, 0
    water_trapped = 0
    while left < right:
        if height[left] < height[right]:
            if height[left] >= left_max:
                left_max = height[left]
            else:
                water_trapped += left_max - height[left]
            left += 1
        else:
            if height[right] >= right_max:
                right_max = height[right]
            else:
                water_trapped += right_max - height[right]
            right -= 1
    return water_trapped

# Example usage
height = [0, 1, 0, 2, 1, 0, 1, 3, 2, 1, 2, 1]
result = trap(height)
print("Trapping Rain Water:", result)  # Output: 6
```

**Explanation:** We use two pointers to find the maximum height on the left and right sides and calculate the water trapped at each position.

### 32. Best Time to Buy and Sell Stock III

**Problem:** You are given an array `prices` where `prices[i]` is the price of a given stock on the `i-th` day. Find the maximum profit you can achieve. You may complete at most two transactions.

**Solution:**

```python
def max_profit_iii(prices):
    if not prices:
        return 0
    first_buy = second_buy = float('inf')
    first_profit = second_profit = 0
    for price in prices:
        first_buy = min(first_buy, price)
        first_profit = max(first_profit, price - first_buy)
        second_buy = min(second_buy, price - first_profit)
        second_profit = max(second_profit, price - second_buy)
    return second_profit

# Example usage
prices = [3, 3, 5, 0, 0, 3, 1, 4]
result = max_profit_iii(prices)
print("Best Time to Buy and Sell Stock III:", result)  # Output: 6
```

**Explanation:** We keep track of the minimum prices for the first and second buys and calculate the maximum profits for the first and second sales.

### 33. First Missing Positive

**Problem:** Given an unsorted integer array `nums`, find the smallest missing positive integer.

**Solution:**

```python
def first_missing_positive(nums):
    n = len(nums)
    for i in range(n):
        while 1 <= nums[i] <= n and nums[nums[i] - 1] != nums[i]:
            nums[nums[i] - 1], nums[i] = nums[i], nums[nums[i] - 1]
    for i in range(n):
        if nums[i] != i + 1:
            return i + 1
    return n + 1

# Example usage
nums = [1, 2, 0]
result = first_missing_positive(nums)
print("First Missing Positive:", result)  # Output: 3
```

**Explanation:** We place each number in its correct position and then find the first missing positive integer.

### 34. Median of Two Sorted Arrays

**Problem:** Given two sorted arrays `nums1` and `nums2` of size `m` and `n` respectively, return the median of the two sorted arrays.

**Solution:**

```python
def find_median_sorted_arrays(nums1, nums2):
    nums = sorted(nums1 + nums2)
    n = len(nums)
    if n % 2 == 1:
        return nums[n // 2]
    else:
        return (nums[n // 2 - 1] + nums[n // 2]) / 2

# Example usage
nums1 = [1, 3]
nums2 = [2]
result = find_median_sorted_arrays(nums1, nums2)
print("Median of Two Sorted Arrays:", result)  # Output: 2.0
```

**Explanation:** We merge the two arrays, sort them, and find the median.

### 35. Jump Game II

**Problem:** Given an array of non-negative integers `nums`, you are initially positioned at the first index of the array. Each element in the array represents your maximum jump length at that position. Your goal is to reach the last index in the minimum number of jumps.

**Solution:**

```python
def jump(nums):
    n = len(nums)
    if n == 1:
        return 0
    jumps = 0
    current_end = 0
    farthest = 0
    for i in range(n - 1):
        farthest = max(farthest, i + nums[i])
        if i == current_end:
            jumps += 1
            current_end = farthest
            if current_end >= n - 1:
                break
    return jumps

# Example usage
nums = [2, 3, 1, 1, 4]
result = jump(nums)
print("Jump Game II:", result)  # Output: 2
```

**Explanation:** We use a greedy approach to determine the minimum number of jumps needed to reach the end of the array.

### 36. Longest Consecutive Sequence

**Problem:** Given an unsorted array of integers `nums`, return the length of the longest consecutive elements sequence.

**Solution:**

```python
def longest_consecutive(nums):
    num_set = set(nums)
    longest_streak = 0
    for num in num_set:
        if num - 1 not in num_set:
            current_num = num
            current_streak = 1
            while current_num + 1 in num_set:
                current_num += 1
                current_streak += 1
            longest_streak = max(longest_streak, current_streak)
    return longest_streak

# Example usage
nums = [100, 4, 200, 1, 3, 2]
result = longest_consecutive(nums)
print("Longest Consecutive Sequence:", result)  # Output: 4
```

**Explanation:** We use a set to store the numbers and find the longest consecutive sequence by checking for the start of each sequence.

### 37. Minimum Window Substring

**Problem:** Given two strings `s` and `t`, return the minimum window in `s` which will contain all the characters in `t`.

**Solution:**

```python
from collections import Counter

def min_window(s, t):
    if not t or not s:
        return ""
    dict_t = Counter(t)
    required = len(dict_t)
    l, r = 0, 0
    formed = 0
    window_counts = {}
    ans = float("inf"), None, None
    while r < len(s):
        character = s[r]
        window_counts[character] = window_counts.get(character, 0) + 1
        if character in dict_t and window_counts[character] == dict_t[character]:
            formed += 1
        while l <= r and formed == required:
            character = s[l]
            if r - l + 1 < ans[0]:
                ans = (r - l + 1, l, r)
            window_counts[character] -= 1
            if character in dict_t and window_counts[character] < dict_t[character]:
                formed -= 1
            l += 1
        r += 1
    return "" if ans[0] == float("inf") else s[ans[1]:ans[2] + 1]

# Example usage
s = "ADOBECODEBANC"
t = "ABC"
result = min_window(s, t)
print("Minimum Window Substring:", result)  # Output: "BANC"
```

**Explanation:** We use a sliding window to find the minimum window that contains all the characters in `t`.

### 38. Gas Station

**Problem:** There are `n` gas stations along a circular route, where the amount of gas at the `i-th` station is `gas[i]`. You have a car with an unlimited gas tank and it costs `cost[i]` of gas to travel from the `i-th` station to its next `(i + 1)-th` station. You begin the journey with an empty tank at one of the gas stations. Return the starting gas station's index if you can travel around the circuit once in the clockwise direction, otherwise return `-1`.

**Solution:**

```python
def can_complete_circuit(gas, cost):
    n = len(gas)
    total_tank, current_tank = 0, 0
    starting_station = 0
    for i in range(n):
        total_tank += gas[i] - cost[i]
        current_tank += gas[i] - cost[i]
        if current_tank < 0:
            starting_station = i + 1
            current_tank = 0
    return starting_station if total_tank >= 0 else -1

# Example usage
gas = [1, 2, 3, 4, 5]
cost = [3, 4, 5, 1, 2]
result = can_complete_circuit(gas, cost)
print("Gas Station:", result)  # Output: 3
```

**Explanation:** We use a greedy approach to find the starting gas station from which we can complete the circuit.

### 39. Meeting Rooms II

**Problem:** Given an array of meeting time intervals `intervals` where `intervals[i] = [starti, endi]`, return the minimum number of conference rooms required.

**Solution:**

```python
import heapq

def min_meeting_rooms(intervals):
    if not intervals:
        return 0
    intervals.sort(key=lambda x: x[0])
    heap = []
    heapq.heappush(heap, intervals[0][1])
    for i in range(1, len(intervals)):
        if intervals[i][0] >= heap[0]:
            heapq.heappop(heap)
        heapq.heappush(heap, intervals[i][1])
    return len(heap)

# Example usage
intervals = [[0, 30], [5, 10], [15, 20]]
result = min_meeting_rooms(intervals)
print("Meeting Rooms II:", result)  # Output: 2
```

**Explanation:** We use a min-heap to keep track of the end times of the meetings and determine the minimum number of rooms required.

### 40. Best Time to Buy and Sell Stock IV

**Problem:** You are given an integer array `prices` where `prices[i]` is the price of a given stock on the `i-th` day, and an integer `k`. Find the maximum profit you can achieve. You may complete at most `k` transactions.

**Solution:**

```python
def max_profit_iv(k, prices):
    if not prices or k == 0:
        return 0
    n = len(prices)
    if k >= n // 2:
        return sum(max(prices[i] - prices[i - 1], 0) for i in range(1, n))
    dp = [[0] * n for _ in range(k + 1)]
    for t in range(1, k + 1):
        max_diff = -prices[0]
        for d in range(1, n):
            dp[t][d] = max(dp[t][d - 1], prices[d] + max_diff)
            max_diff = max(max_diff, dp[t - 1][d] - prices[d])
    return dp[k][n - 1]

# Example usage
k = 2
prices = [3, 2, 6, 5, 0, 3]
result = max_profit_iv(k, prices)
print("Best Time to Buy and Sell Stock IV:", result)  # Output: 7
```

**Explanation:** We use dynamic programming to find the maximum profit with at most `k` transactions.

### 41. First Bad Version

**Problem:** You are a product manager and currently leading a team to develop a new product. Unfortunately, the latest version of your product fails the quality check. Since each version is developed based on the previous version, all the versions after a bad version are also bad. Suppose you have `n` versions `[1, 2, ..., n]` and you want to find out the first bad one, which causes all the following ones to be bad.

**Solution:**

```python
def first_bad_version(n):
    def is_bad_version(version):
        # This is a mock function. The actual implementation would check if the version is bad.
        return version >= 4

    left, right = 1, n
    while left < right:
        mid = (left + right) // 2
        if is_bad_version(mid):
            right = mid
        else:
            left = mid + 1
    return left

# Example usage
n = 5
result = first_bad_version(n)
print("First Bad Version:", result)  # Output: 4
```

**Explanation:** We use binary search to find the first bad version.

### 42. Search Insert Position

**Problem:** Given a sorted array of distinct integers and a target value, return the index if the target is found. If not, return the index where it would be if it were inserted in order.

**Solution:**

```python
def search_insert(nums, target):
    left, right = 0, len(nums) - 1
    while left <= right:
        mid = (left + right) // 2
        if nums[mid] == target:
            return mid
        elif nums[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    return left

# Example usage
nums = [1, 3, 5, 6]
target = 5
result = search_insert(nums, target)
print("Search Insert Position:", result)  # Output: 2
```

**Explanation:** We use binary search to find the insert position of the target.

### 43. Guess Number Higher or Lower

**Problem:** We are playing the Guess Game. The game is as follows: I pick a number from 1 to `n`. You have to guess which number I picked. Every time you guess wrong, I will tell you whether the number I picked is higher or lower.

**Solution:**

```python
def guess_number(n):
    def guess(num):
        # This is a mock function. The actual implementation would check if the guess is correct.
        pick = 6
        if num < pick:
            return 1
        elif num > pick:
            return -1
        else:
            return 0

    left, right = 1, n
    while left <= right:
        mid = (left + right) // 2
        result = guess(mid)
        if result == 0:
            return mid
        elif result == 1:
            left = mid + 1
        else:
            right = mid - 1
    return -1

# Example usage
n = 10
result = guess_number(n)
print("Guess Number Higher or Lower:", result)  # Output: 6
```

**Explanation:** We use binary search to guess the number.

### 44. Peak Index in a Mountain Array

**Problem:** Let's call an array `arr` a mountain if the following properties hold: `arr.length >= 3`, there exists some `i` with `0 < i < arr.length - 1` such that `arr[0] < arr[1] < ... arr[i-1] < arr[i] > arr[i+1] > ... > arr[arr.length - 1]`. Given an integer array `arr` that is guaranteed to be a mountain, return any `i` such that `arr[0] < arr[1] < ... arr[i-1] < arr[i] > arr[i+1] > ... > arr[arr.length - 1]`.

**Solution:**

```python
def peak_index_in_mountain_array(arr):
    left, right = 0, len(arr) - 1
    while left < right:
        mid = (left + right) // 2
        if arr[mid] < arr[mid + 1]:
            left = mid + 1
        else:
            right = mid
    return left

# Example usage
arr = [0, 1, 0]
result = peak_index_in_mountain_array(arr)
print("Peak Index in a Mountain Array:", result)  # Output: 1
```

**Explanation:** We use binary search to find the peak index in the mountain array.

### 45. Search a 2D Matrix II

**Problem:** Write an efficient algorithm that searches for a value `target` in an `m x n` integer matrix `matrix`. This matrix has the following properties: Integers in each row are sorted in ascending from left to right. Integers in each column are sorted in ascending from top to bottom.

**Solution:**

```python
def search_matrix(matrix, target):
    if not matrix or not matrix[0]:
        return False
    rows, cols = len(matrix), len(matrix[0])
    row, col = 0, cols - 1
    while row < rows and col >= 0:
        if matrix[row][col] == target:
            return True
        elif matrix[row][col] < target:
            row += 1
        else:
            col -= 1
    return False

# Example usage
matrix = [
    [1, 4, 7, 11, 15],
    [2, 5, 8, 12, 19],
    [3, 6, 9, 16, 22],
    [10, 13, 14, 17, 24],
    [18, 21, 23, 26, 30]
]
target = 5
result = search_matrix(matrix, target)
print("Search a 2D Matrix II:", result)  # Output: True
```

**Explanation:** We start from the top-right corner and move left or down based on the comparison with the target.

### 46. Find Minimum in Rotated Sorted Array

**Problem:** Suppose an array of length `n` sorted in ascending order is rotated between `1` and `n` times. For example, the array `nums = [0, 1, 2, 4, 5, 6, 7]` might become: `[4, 5, 6, 7, 0, 1, 2]` if it was rotated `4` times. Given the sorted rotated array `nums` of unique elements, return the minimum element of this array.

**Solution:**

```python
def find_min(nums):
    left, right = 0, len(nums) - 1
    while left < right:
        mid = (left + right) // 2
        if nums[mid] > nums[right]:
            left = mid + 1
        else:
            right = mid
    return nums[left]

# Example usage
nums = [3, 4, 5, 1, 2]
result = find_min(nums)
print("Find Minimum in Rotated Sorted Array:", result)  # Output: 1
```

**Explanation:** We use binary search to find the minimum element in the rotated sorted array.

### 47. Find K Closest Elements

**Problem:** Given a sorted integer array `arr`, two integers `k` and `x`, return the `k` closest integers to `x` in the array. The result should also be sorted in ascending order.

**Solution:**

```python
import bisect

def find_closest_elements(arr, k, x):
    pos = bisect.bisect_left(arr, x)
    left, right = pos - 1, pos
    result = []
    while k > 0:
        if left < 0:
            result.append(arr[right])
            right += 1
        elif right >= len(arr):
            result.append(arr[left])
            left -= 1
        elif abs(arr[left] - x) <= abs(arr[right] - x):
            result.append(arr[left])
            left -= 1
        else:
            result.append(arr[right])
            right += 1
        k -= 1
    return sorted(result)

# Example usage
arr = [1, 2, 3, 4, 5]
k = 4
x = 3
result = find_closest_elements(arr, k, x)
print("Find K Closest Elements:", result)  # Output: [1, 2, 3, 4]
```

**Explanation:** We use binary search to find the position of `x` and then use two pointers to find the `k` closest elements.

### 48. First Missing Positive

**Problem:** Given an unsorted integer array `nums`, find the smallest missing positive integer.

**Solution:**

```python
def first_missing_positive(nums):
    n = len(nums)
    for i in range(n):
        while 1 <= nums[i] <= n and nums[nums[i] - 1] != nums[i]:
            nums[nums[i] - 1], nums[i] = nums[i], nums[nums[i] - 1]
    for i in range(n):
        if nums[i] != i + 1:
            return i + 1
    return n + 1

# Example usage
nums = [1, 2, 0]
result = first_missing_positive(nums)
print("First Missing Positive:", result)  # Output: 3
```

**Explanation:** We place each number in its correct position and then find the first missing positive integer.

### 49. Search in Rotated Sorted Array

**Problem:** Given the sorted rotated array `nums` of unique elements, return the index of the target if it is in `nums`, or `-1` if it is not in `nums`.

**Solution:**

```python
def search(nums, target):
    left, right = 0, len(nums) - 1
    while left <= right:
        mid = (left + right) // 2
        if nums[mid] == target:
            return mid
        if nums[left] <= nums[mid]:
            if nums[left] <= target < nums[mid]:
                right = mid - 1
            else:
                left = mid + 1
        else:
            if nums[mid] < target <= nums[right]:
                left = mid + 1
            else:
                right = mid - 1
    return -1

# Example usage
nums = [4, 5, 6, 7, 0, 1, 2]
target = 0
result = search(nums, target)
print("Search in Rotated Sorted Array:", result)  # Output: 4
```

**Explanation:** We use binary search to find the target in a rotated sorted array.

### 50. Search a 2D Matrix

**Problem:** Write an efficient algorithm that searches for a value `target` in an `m x n` integer matrix `matrix`. This matrix has the following properties: Integers in each row are sorted in ascending from left to right. Integers in each column are sorted in ascending from top to bottom.

**Solution:**

```python
def search_matrix(matrix, target):
    if not matrix or not matrix[0]:
        return False
    rows, cols = len(matrix), len(matrix[0])
    left, right = 0, rows * cols - 1
    while left <= right:
        mid = (left + right) // 2
        mid_value = matrix[mid // cols][mid % cols]
        if mid_value == target:
            return True
        elif mid_value < target:
            left = mid + 1
        else:
            right = mid - 1
    return False

# Example usage
matrix = [
    [1, 3, 5, 7],
    [10, 11, 16, 20],
    [23, 30, 34, 60]
]
target = 3
result = search_matrix(matrix, target)
print("Search a 2D Matrix:", result)  # Output: True
```

**Explanation:** We use binary search to find the target in a 2D matrix.

### 51. Divide Two Integers

**Problem:** Given two integers `dividend` and `divisor`, divide two integers without using multiplication, division, and mod operator.

**Solution:**

```python
def divide(dividend, divisor):
    if dividend == 0:
        return 0
    if divisor == 0:
        return float('inf')
    negative = (dividend < 0) != (divisor < 0)
    dividend, divisor = abs(dividend), abs(divisor)
    quotient = 0
    while dividend >= divisor:
        temp, multiple = divisor, 1
        while dividend >= temp:
            dividend -= temp
            quotient += multiple
            temp += temp
            multiple += multiple
    if negative:
        quotient = -quotient
    return min(max(-2**31, quotient), 2**31 - 1)

# Example usage
dividend = 10
divisor = 3
result = divide(dividend, divisor)
print("Divide Two Integers:", result)  # Output: 3
```

**Explanation:** We use repeated subtraction to divide the two integers.

### 52. Median of Two Sorted Arrays

**Problem:** Given two sorted arrays `nums1` and `nums2` of size `m` and `n` respectively, return the median of the two sorted arrays.

**Solution:**

```python
def find_median_sorted_arrays(nums1, nums2):
    nums = sorted(nums1 + nums2)
    n = len(nums)
    if n % 2 == 1:
        return nums[n // 2]
    else:
        return (nums[n // 2 - 1] + nums[n // 2]) / 2

# Example usage
nums1 = [1, 3]
nums2 = [2]
result = find_median_sorted_arrays(nums1, nums2)
print("Median of Two Sorted Arrays:", result)  # Output: 2.0
```

**Explanation:** We merge the two arrays, sort them, and find the median.

### 53. Find Peak Element

**Problem:** A peak element is an element that is greater than its neighbors. Given an input array `nums`, where `nums[i] != nums[i + 1]`, find a peak element and return its index.

**Solution:**

```python
def find_peak_element(nums):
    left, right = 0, len(nums) - 1
    while left < right:
        mid = (left + right) // 2
        if nums[mid] > nums[mid + 1]:
            right = mid
        else:
            left = mid + 1
    return left

# Example usage
nums = [1, 2, 3, 1]
result = find_peak_element(nums)
print("Find Peak Element:", result)  # Output: 2
```

**Explanation:** We use binary search to find a peak element in the array.

### 54. Find Kth Smallest Element in a Sorted Matrix

**Problem:** Given an `n x n` matrix where each of the rows and columns is sorted in ascending order, return the `k-th` smallest element in the matrix.

**Solution:**

```python
import heapq

def kth_smallest(matrix, k):
    min_heap = []
    for i in range(len(matrix)):
        heapq.heappush(min_heap, (matrix[i][0], i, 0))
    count, result = 0, 0
    while min_heap:
        val, i, j = heapq.heappop(min_heap)
        count += 1
        if count == k:
            result = val
            break
        if j + 1 < len(matrix[0]):
            heapq.heappush(min_heap, (matrix[i][j + 1], i, j + 1))
    return result

# Example usage
matrix = [
    [1, 5, 9],
    [10, 11, 13],
    [12, 13, 15]
]
k = 8
result = kth_smallest(matrix, k)
print("Find Kth Smallest Element in a Sorted Matrix:", result)  # Output: 13
```

**Explanation:** We use a min-heap to find the `k-th` smallest element in the matrix.

### 55. Search in Rotated Sorted Array II

**Problem:** Given the sorted rotated array `nums` that may contain duplicates, return `true` if `target` is in `nums`, or `false` if it is not in `nums`.

**Solution:**

```python
def search(nums, target):
    left, right = 0, len(nums) - 1
    while left <= right:
        mid = (left + right) // 2
        if nums[mid] == target:
            return True
        if nums[left] == nums[mid] == nums[right]:
            left += 1
            right -= 1
        elif nums[left] <= nums[mid]:
            if nums[left] <= target < nums[mid]:
                right = mid - 1
            else:
                left = mid + 1
        else:
            if nums[mid] < target <= nums[right]:
                left = mid + 1
            else:
                right = mid - 1
    return False

# Example usage
nums = [2, 5, 6, 0, 0, 1, 2]
target = 0
result = search(nums, target)
print("Search in Rotated Sorted Array II:", result)  # Output: True
```

**Explanation:** We use binary search to find the target in a rotated sorted array with duplicates.

### 56. Find First and Last Position of Element in Sorted Array

**Problem:** Given an array of integers `nums` sorted in ascending order, find the starting and ending position of a given `target` value.

**Solution:**

```python
def search_range(nums, target):
    def binary_search_left(nums, target):
        left, right = 0, len(nums) - 1
        while left <= right:
            mid = (left + right) // 2
            if nums[mid] < target:
                left = mid + 1
            else:
                right = mid - 1
        return left

    def binary_search_right(nums, target):
        left, right = 0, len(nums) - 1
        while left <= right:
            mid = (left + right) // 2
            if nums[mid] <= target:
                left = mid + 1
            else:
                right = mid - 1
        return right

    left_index = binary_search_left(nums, target)
    right_index = binary_search_right(nums, target)
    if left_index <= right_index:
        return [left_index, right_index]
    return [-1, -1]

# Example usage
nums = [5, 7, 7, 8, 8, 10]
target = 8
result = search_range(nums, target)
print("Find First and Last Position of Element in Sorted Array:", result)  # Output: [3, 4]
```

**Explanation:** We use binary search to find the leftmost and rightmost positions of the target in the sorted array.

### 57. First Missing Positive

**Problem:** Given an unsorted integer array `nums`, find the smallest missing positive integer.

**Solution:**

```python
def first_missing_positive(nums):
    n = len(nums)
    for i in range(n):
        while 1 <= nums[i] <= n and nums[nums[i] - 1] != nums[i]:
            nums[nums[i] - 1], nums[i] = nums[i], nums[nums[i] - 1]
    for i in range(n):
        if nums[i] != i + 1:
            return i + 1
    return n + 1

# Example usage
nums = [1, 2, 0]
result = first_missing_positive(nums)
print("First Missing Positive:", result)  # Output: 3
```

**Explanation:** We place each number in its correct position and then find the first missing positive integer.

### 58. Search a 2D Matrix II

**Problem:** Write an efficient algorithm that searches for a value `target` in an `m x n` integer matrix `matrix`. This matrix has the following properties: Integers in each row are sorted in ascending from left to right. Integers in each column are sorted in ascending from top to bottom.

**Solution:**

```python
def search_matrix(matrix, target):
    if not matrix or not matrix[0]:
        return False
    rows, cols = len(matrix), len(matrix[0])
    row, col = 0, cols - 1
    while row < rows and col >= 0:
        if matrix[row][col] == target:
            return True
        elif matrix[row][col] < target:
            row += 1
        else:
            col -= 1
    return False

# Example usage
matrix = [
    [1, 4, 7, 11, 15],
    [2, 5, 8, 12, 19],
    [3, 6, 9, 16, 22],
    [10, 13, 14, 17, 24],
    [18, 21, 23, 26, 30]
]
target = 5
result = search_matrix(matrix, target)
print("Search a 2D Matrix II:", result)  # Output: True
```

**Explanation:** We start from the top-right corner and move left or down based on the comparison with the target.

### 59. Search Insert Position

**Problem:** Given a sorted array of distinct integers and a target value, return the index if the target is found. If not, return the index where it would be if it were inserted in order.

**Solution:**

```python
def search_insert(nums, target):
    left, right = 0, len(nums) - 1
    while left <= right:
        mid = (left + right) // 2
        if nums[mid] == target:
            return mid
        elif nums[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    return left

# Example usage
nums = [1, 3, 5, 6]
target = 5
result = search_insert(nums, target)
print("Search Insert Position:", result)  # Output: 2
```

**Explanation:** We use binary search to find the insert position of the target.

### 60. Search in Rotated Sorted Array

**Problem:** Given the sorted rotated array `nums` of unique elements, return the index of the target if it is in `nums`, or `-1` if it is not in `nums`.

**Solution:**

```python
def search(nums, target):
    left, right = 0, len(nums) - 1
    while left <= right:
        mid = (left + right) // 2
        if nums[mid] == target:
            return mid
        if nums[left] <= nums[mid]:
            if nums[left] <= target < nums[mid]:
                right = mid - 1
            else:
                left = mid + 1
        else:
            if nums[mid] < target <= nums[right]:
                left = mid + 1
            else:
                right = mid - 1
    return -1

# Example usage
nums = [4, 5, 6, 7, 0, 1, 2]
target = 0
result = search(nums, target)
print("Search in Rotated Sorted Array:", result)  # Output: 4
```

**Explanation:** We use binary search to find the target in a rotated sorted array.

### 61. Search in Rotated Sorted Array II

**Problem:** Given the sorted rotated array `nums` that may contain duplicates, return `true` if `target` is in `nums`, or `false` if it is not in `nums`.

**Solution:**

```python
def search(nums, target):
    left, right = 0, len(nums) - 1
    while left <= right:
        mid = (left + right) // 2
        if nums[mid] == target:
            return True
        if nums[left] == nums[mid] == nums[right]:
            left += 1
            right -= 1
        elif nums[left] <= nums[mid]:
            if nums[left] <= target < nums[mid]:
                right = mid - 1
            else:
                left = mid + 1
        else:
            if nums[mid] < target <= nums[right]:
                left = mid + 1
            else:
                right = mid - 1
    return False

# Example usage
nums = [2, 5, 6, 0, 0, 1, 2]
target = 0
result = search(nums, target)
print("Search in Rotated Sorted Array II:", result)  # Output: True
```

**Explanation:** We use binary search to find the target in a rotated sorted array with duplicates.

### 62. Median of Two Sorted Arrays

**Problem:** Given two sorted arrays `nums1` and `nums2` of size `m` and `n` respectively, return the median of the two sorted arrays.

**Solution:**

```python
def find_median_sorted_arrays(nums1, nums2):
    nums = sorted(nums1 + nums2)
    n = len(nums)
    if n % 2 == 1:
        return nums[n // 2]
    else:
        return (nums[n // 2 - 1] + nums[n // 2]) / 2

# Example usage
nums1 = [1, 3]
nums2 = [2]
result = find_median_sorted_arrays(nums1, nums2)
print("Median of Two Sorted Arrays:", result)  # Output: 2.0
```

**Explanation:** We merge the two arrays, sort them, and find the median.

### 63. Search a 2D Matrix II

**Problem:** Write an efficient algorithm that searches for a value `target` in an `m x n` integer matrix `matrix`. This matrix has the following properties: Integers in each row are sorted in ascending from left to right. Integers in each column are sorted in ascending from top to bottom.

**Solution:**

```python
def search_matrix(matrix, target):
    if not matrix or not matrix[0]:
        return False
    rows, cols = len(matrix), len(matrix[0])
    row, col = 0, cols - 1
    while row < rows and col >= 0:
        if matrix[row][col] == target:
            return True
        elif matrix[row][col] < target:
            row += 1
        else:
            col -= 1
    return False

# Example usage
matrix = [
    [1, 4, 7, 11, 15],
    [2, 5, 8, 12, 19],
    [3, 6, 9, 16, 22],
    [10, 13, 14, 17, 24],
    [18, 21, 23, 26, 30]
]
target = 5
result = search_matrix(matrix, target)
print("Search a 2D Matrix II:", result)  # Output: True
```

**Explanation:** We start from the top-right corner and move left or down based on the comparison with the target.

### 64. Find Minimum in Rotated Sorted Array

**Problem:** Suppose an array of length `n` sorted in ascending order is rotated between `1` and `n` times. For example, the array `nums = [0, 1, 2, 4, 5, 6, 7]` might become: `[4, 5, 6, 7, 0, 1, 2]` if it was rotated `4` times. Given the sorted rotated array `nums` of unique elements, return the minimum element of this array.

**Solution:**

```python
def find_min(nums):
    left, right = 0, len(nums) - 1
    while left < right:
        mid = (left + right) // 2
        if nums[mid] > nums[right]:
            left = mid + 1
        else:
            right = mid
    return nums[left]

# Example usage
nums = [3, 4, 5, 1, 2]
result = find_min(nums)
print("Find Minimum in Rotated Sorted Array:", result)  # Output: 1
```

**Explanation:** We use binary search to find the minimum element in the rotated sorted array.

### 65. Search in Rotated Sorted Array

**Problem:** Given the sorted rotated array `nums` of unique elements, return the index of the target if it is in `nums`, or `-1` if it is not in `nums`.

**Solution:**

```python
def search(nums, target):
    left, right = 0, len(nums) - 1
    while left <= right:
        mid = (left + right) // 2
        if nums[mid] == target:
            return mid
        if nums[left] <= nums[mid]:
            if nums[left] <= target < nums[mid]:
                right = mid - 1
            else:
                left = mid + 1
        else:
            if nums[mid] < target <= nums[right]:
                left = mid + 1
            else:
                right = mid - 1
    return -1

# Example usage
nums = [4, 5, 6, 7, 0, 1, 2]
target = 0
result = search(nums, target)
print("Search in Rotated Sorted Array:", result)  # Output: 4
```

**Explanation:** We use binary search to find the target in a rotated sorted array.

### 66. First Missing Positive

**Problem:** Given an unsorted integer array `nums`, find the smallest missing positive integer.

**Solution:**

```python
def first_missing_positive(nums):
    n = len(nums)
    for i in range(n):
        while 1 <= nums[i] <= n and nums[nums[i] - 1] != nums[i]:
            nums[nums[i] - 1], nums[i] = nums[i], nums[nums[i] - 1]
    for i in range(n):
        if nums[i] != i + 1:
            return i + 1
    return n + 1

# Example usage
nums = [1, 2, 0]
result = first_missing_positive(nums)
print("First Missing Positive:", result)  # Output: 3
```

**Explanation:** We place each number in its correct position and then find the first missing positive integer.

### 67. Search Insert Position

**Problem:** Given a sorted array of distinct integers and a target value, return the index if the target is found. If not, return the index where it would be if it were inserted in order.

**Solution:**

```python
def search_insert(nums, target):
    left, right = 0, len(nums) - 1
    while left <= right:
        mid = (left + right) // 2
        if nums[mid] == target:
            return mid
        elif nums[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    return left

# Example usage
nums = [1, 3, 5, 6]
target = 5
result = search_insert(nums, target)
print("Search Insert Position:", result)  # Output: 2
```

**Explanation:** We use binary search to find the insert position of the target.

### 68. Find Peak Element

**Problem:** A peak element is an element that is greater than its neighbors. Given an input array `nums`, where `nums[i] != nums[i + 1]`, find a peak element and return its index.

**Solution:**

```python
def find_peak_element(nums):
    left, right = 0, len(nums) - 1
    while left < right:
        mid = (left + right) // 2
        if nums[mid] > nums[mid + 1]:
            right = mid
        else:
            left = mid + 1
    return left

# Example usage
nums = [1, 2, 3, 1]
result = find_peak_element(nums)
print("Find Peak Element:", result)  # Output: 2
```

**Explanation:** We use binary search to find a peak element in the array.

### 69. First Bad Version

**Problem:** You are a product manager and currently leading a team to develop a new product. Unfortunately, the latest version of your product fails the quality check. Since each version is developed based on the previous version, all the versions after a bad version are also bad. Suppose you have `n` versions `[1, 2, ..., n]` and you want to find out the first bad one, which causes all the following ones to be bad.

**Solution:**

```python
def first_bad_version(n):
    def is_bad_version(version):
        # This is a mock function. The actual implementation would check if the version is bad.
        return version >= 4

    left, right = 1, n
    while left < right:
        mid = (left + right) // 2
        if is_bad_version(mid):
            right = mid
        else:
            left = mid + 1
    return left

# Example usage
n = 5
result = first_bad_version(n)
print("First Bad Version:", result)  # Output: 4
```

**Explanation:** We use binary search to find the first bad version.

### 70. Find First and Last Position of Element in Sorted Array

**Problem:** Given an array of integers `nums` sorted in ascending order, find the starting and ending position of a given `target` value.

**Solution:**

```python
def search_range(nums, target):
    def binary_search_left(nums, target):
        left, right = 0, len(nums) - 1
        while left <= right:
            mid = (left + right) // 2
            if nums[mid] < target:
                left = mid + 1
            else:
                right = mid - 1
        return left

    def binary_search_right(nums, target):
        left, right = 0, len(nums) - 1
        while left <= right:
            mid = (left + right) // 2
            if nums[mid] <= target:
                left = mid + 1
            else:
                right = mid - 1
        return right

    left_index = binary_search_left(nums, target)
    right_index = binary_search_right(nums, target)
    if left_index <= right_index:
        return [left_index, right_index]
    return [-1, -1]

# Example usage
nums = [5, 7, 7, 8, 8, 10]
target = 8
result = search_range(nums, target)
print("Find First and Last Position of Element in Sorted Array:", result)  # Output: [3, 4]
```

**Explanation:** We use binary search to find the leftmost and rightmost positions of the target in the sorted array.

### 71. Climbing Stairs

**Problem:** You are climbing a staircase. It takes `n` steps to reach the top. Each time you can either climb `1` or `2` steps. In how many distinct ways can you climb to the top?

**Solution:**

```python
def climb_stairs(n):
    if n == 1:
        return 1
    if n == 2:
        return 2
    prev1, prev2 = 1, 2
    for i in range(3, n + 1):
        current = prev1 + prev2
        prev1, prev2 = prev2, current
    return prev2

# Example usage
n = 3
result = climb_stairs(n)
print("Climbing Stairs:", result)  # Output: 3
```

**Explanation:** We use dynamic programming to find the number of distinct ways to climb the stairs.

### 72. Fibonacci Number

**Problem:** The Fibonacci numbers, commonly denoted `F(n)` form a sequence, called the Fibonacci sequence, such that each number is the sum of the two preceding ones, starting from `0` and `1`. That is, `F(0) = 0`, `F(1) = 1`, `F(n) = F(n - 1) + F(n - 2)`, for `n > 1`. Given `n`, calculate `F(n)`.

**Solution:**

```python
def fib(n):
    if n == 0:
        return 0
    if n == 1:
        return 1
    prev1, prev2 = 0, 1
    for i in range(2, n + 1):
        current = prev1 + prev2
        prev1, prev2 = prev2, current
    return prev2

# Example usage
n = 4
result = fib(n)
print("Fibonacci Number:", result)  # Output: 3
```

**Explanation:** We use dynamic programming to calculate the `n-th` Fibonacci number.

### 73. Reverse String

**Problem:** Write a function that reverses a string. The input string is given as an array of characters `s`.

**Solution:**

```python
def reverse_string(s):
    left, right = 0, len(s) - 1
    while left < right:
        s[left], s[right] = s[right], s[left]
        left += 1
        right -= 1
    return s

# Example usage
s = ["h", "e", "l", "l", "o"]
result = reverse_string(s)
print("Reverse String:", result)  # Output: ['o', 'l', 'l', 'e', 'h']
```

**Explanation:** We use two pointers to reverse the string in place.

### 74. Pow(x, n)

**Problem:** Implement `pow(x, n)`, which calculates `x` raised to the power `n` (i.e., `xn`).

**Solution:**

```python
def my_pow(x, n):
    if n == 0:
        return 1
    if n < 0:
        x = 1 / x
        n = -n
    result = 1
    while n > 0:
        if n % 2 == 1:
            result *= x
        x *= x
        n //= 2
    return result

# Example usage
x = 2.0
n = 10
result = my_pow(x, n)
print("Pow(x, n):", result)  # Output: 1024.0
```

**Explanation:** We use iterative method with exponentiation by squaring to calculate the power.

### 75. Merge Two Sorted Lists

**Problem:** Merge two sorted linked lists and return it as a sorted list. The list should be made by splicing together the nodes of the first two lists.

**Solution:**

```python
class ListNode:
    def __init__(self, val=0, next=None):
        self.val = val
        self.next = next

def merge_two_lists(l1, l2):
    dummy = ListNode()
    current = dummy
    while l1 and l2:
        if l1.val < l2.val:
            current.next = l1
            l1 = l1.next
        else:
            current.next = l2
            l2 = l2.next
        current = current.next
    current.next = l1 or l2
    return dummy.next

# Example usage
l1 = ListNode(1, ListNode(2, ListNode(4)))
l2 = ListNode(1, ListNode(3, ListNode(4)))
result = merge_two_lists(l1, l2)
# Output: [1, 1, 2, 3, 4, 4]
```

**Explanation:** We merge the two linked lists by comparing the values of the nodes and adjusting the pointers accordingly.

### 76. Maximum Depth of Binary Tree

**Problem:** Given the `root` of a binary tree, return its maximum depth.

**Solution:**

```python
class TreeNode:
    def __init__(self, val=0, left=None, right=None):
        self.val = val
        self.left = left
        self.right = right

def max_depth(root):
    if not root:
        return 0
    left_depth = max_depth(root.left)
    right_depth = max_depth(root.right)
    return max(left_depth, right_depth) + 1

# Example usage
root = TreeNode(3, TreeNode(9), TreeNode(20, TreeNode(15), TreeNode(7)))
result = max_depth(root)
print("Maximum Depth of Binary Tree:", result)  # Output: 3
```

**Explanation:** We use recursion to find the maximum depth of the binary tree.

### 77. Symmetric Tree

**Problem:** Given the `root` of a binary tree, check whether it is a mirror of itself (i.e., symmetric around its center).

**Solution:**

```python
def is_symmetric(root):
    def is_mirror(t1, t2):
        if not t1 and not t2:
            return True
        if not t1 or not t2:
            return False
        return (t1.val == t2.val) and is_mirror(t1.right, t2.left) and is_mirror(t1.left, t2.right)

    return is_mirror(root, root)

# Example usage
root = TreeNode(1, TreeNode(2, TreeNode(3), TreeNode(4)), TreeNode(2, TreeNode(4), TreeNode(3)))
result = is_symmetric(root)
print("Symmetric Tree:", result)  # Output: True
```

**Explanation:** We use recursion to check if the tree is symmetric.

### 78. Path Sum

**Problem:** Given the `root` of a binary tree and an integer `targetSum`, return `true` if the tree has a root-to-leaf path such that adding up all the values along the path equals `targetSum`.

**Solution:**

```python
def has_path_sum(root, targetSum):
    if not root:
        return False
    if not root.left and not root.right:
        return root.val == targetSum
    targetSum -= root.val
    return has_path_sum(root.left, targetSum) or has_path_sum(root.right, targetSum)

# Example usage
root = TreeNode(5, TreeNode(4, TreeNode(11, TreeNode(7), TreeNode(2))), TreeNode(8, TreeNode(13), TreeNode(4, None, TreeNode(1))))
targetSum = 22
result = has_path_sum(root, targetSum)
print("Path Sum:", result)  # Output: True
```

**Explanation:** We use recursion to check if there is a root-to-leaf path with the given sum.

### 79. Subsets

**Problem:** Given an integer array `nums` that may contain duplicates, return all possible subsets (the power set).

**Solution:**

```python
def subsets(nums):
    def backtrack(start, path):
        result.append(path)
        for i in range(start, len(nums)):
            backtrack(i + 1, path + [nums[i]])

    result = []
    backtrack(0, [])
    return result

# Example usage
nums = [1, 2, 3]
result = subsets(nums)
print("Subsets:", result)  # Output: [[], [1], [1, 2], [1, 2, 3], [1, 3], [2], [2, 3], [3]]
```

**Explanation:** We use backtracking to generate all possible subsets.

### 80. Generate Parentheses

**Problem:** Given `n` pairs of parentheses, write a function to generate all combinations of well-formed parentheses.

**Solution:**

```python
def generate_parenthesis(n):
    def backtrack(open_count, close_count, path):
        if open_count == close_count == n:
            result.append(path)
            return
        if open_count < n:
            backtrack(open_count + 1, close_count, path + '(')
        if close_count < open_count:
            backtrack(open_count, close_count + 1, path + ')')

    result = []
    backtrack(0, 0, '')
    return result

# Example usage
n = 3
result = generate_parenthesis(n)
print("Generate Parentheses:", result)  # Output: ['((()))', '(()())', '(())()', '()(())', '()()()']
```

**Explanation:** We use backtracking to generate all combinations of well-formed parentheses.

### 81. Permutations

**Problem:** Given an array `nums` of distinct integers, return all the possible permutations.

**Solution:**

```python
def permute(nums):
    def backtrack(path):
        if len(path) == len(nums):
            result.append(path)
            return
        for num in nums:
            if num not in path:
                backtrack(path + [num])

    result = []
    backtrack([])
    return result

# Example usage
nums = [1, 2, 3]
result = permute(nums)
print("Permutations:", result)  # Output: [[1, 2, 3], [1, 3, 2], [2, 1, 3], [2, 3, 1], [3, 1, 2], [3, 2, 1]]
```

**Explanation:** We use backtracking to generate all possible permutations.

### 82. Combinations

**Problem:** Given two integers `n` and `k`, return all possible combinations of `k` numbers out of the range `[1, n]`.

**Solution:**

```python
def combine(n, k):
    def backtrack(start, path):
        if len(path) == k:
            result.append(path)
            return
        for i in range(start, n + 1):
            backtrack(i + 1, path + [i])

    result = []
    backtrack(1, [])
    return result

# Example usage
n = 4
k = 2
result = combine(n, k)
print("Combinations:", result)  # Output: [[1, 2], [1, 3], [1, 4], [2, 3], [2, 4], [3, 4]]
```

**Explanation:** We use backtracking to generate all possible combinations.

### 83. Palindrome Partitioning

**Problem:** Given a string `s`, partition `s` such that every substring of the partition is a palindrome. Return all possible palindrome partitioning of `s`.

**Solution:**

```python
def partition(s):
    def is_palindrome(substring):
        return substring == substring[::-1]

    def backtrack(start, path):
        if start == len(s):
            result.append(path)
            return
        for end in range(start + 1, len(s) + 1):
            if is_palindrome(s[start:end]):
                backtrack(end, path + [s[start:end]])

    result = []
    backtrack(0, [])
    return result

# Example usage
s = "aab"
result = partition(s)
print("Palindrome Partitioning:", result)  # Output: [['a', 'a', 'b'], ['aa', 'b']]
```

**Explanation:** We use backtracking to generate all possible palindrome partitioning.

### 84. Expression Add Operators

**Problem:** Given a string `num` that contains only digits and an integer `target`, return all possibilities to insert the binary operators `+`, `-`, or `*` between the digits of `num` so that the resultant expression evaluates to the `target` value.

**Solution:**

```python
def add_operators(num, target):
    def backtrack(index, prev_value, current_value, last_operator, path):
        if index == len(num):
            if current_value == target:
                result.append(path)
            return
        for i in range(index, len(num)):
            if i != index and num[index] == '0':
                break
            current = int(num[index:i + 1])
            if index == 0:
                backtrack(i + 1, current, current, '+', path + num[index:i + 1])
            else:
                backtrack(i + 1, current, current_value + current, '+', path + '+' + num[index:i + 1])
                backtrack(i + 1, -current, current_value - current, '-', path + '-' + num[index:i + 1])
                backtrack(i + 1, prev_value * current, current_value - prev_value + prev_value * current, '*', path + '*' + num[index:i + 1])

    result = []
    backtrack(0, 0, 0, '+', '')
    return result

# Example usage
num = "123"
target = 6
result = add_operators(num, target)
print("Expression Add Operators:", result)  # Output: ['1+2+3', '1*2*3']
```

**Explanation:** We use backtracking to generate all possible expressions that evaluate to the target value.

### 85. Word Search

**Problem:** Given an `m x n` grid of characters `board` and a string `word`, return `true` if `word` exists in the grid.

**Solution:**

```python
def exist(board, word):
    def dfs(i, j, word_index):
        if word_index == len(word):
            return True
        if i < 0 or i >= len(board) or j < 0 or j >= len(board[0]) or board[i][j] != word[word_index]:
            return False
        temp = board[i][j]

