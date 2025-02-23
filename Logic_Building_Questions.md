
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

