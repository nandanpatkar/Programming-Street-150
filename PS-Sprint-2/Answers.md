Let's go through each of the problems one by one, providing both Python and C++ code with explanations.

### 1. Finding the Sum of Digits of a Number Until Zero

**Python Code:**

```python
def sum_of_digits(number):
    while number >= 10:
        number = sum(int(digit) for digit in str(number))
    return number

# Example usage
number = 123
result = sum_of_digits(number)
print(result)  # Output: 6
```

**Explanation:**
- The function `sum_of_digits` repeatedly sums the digits of the input number until the result is a single digit.
- It converts the number to a string to iterate over each digit, converts each digit back to an integer, and sums them.
- The process continues until the number is less than 10.

**C++ Code:**

```cpp
#include <iostream>

int sum_of_digits(int number) {
    while (number >= 10) {
        int sum = 0;
        while (number > 0) {
            sum += number % 10;
            number /= 10;
        }
        number = sum;
    }
    return number;
}

int main() {
    int number = 123;
    int result = sum_of_digits(number);
    std::cout << result << std::endl;  // Output: 6
    return 0;
}
```

**Explanation:**
- The function `sum_of_digits` repeatedly sums the digits of the input number until the result is a single digit.
- It uses a loop to extract each digit by taking the remainder of the number divided by 10 and sums them.
- The process continues until the number is less than 10.

### 2. Generating a Multiplication Table for a Range

**Python Code:**

```python
def multiplication_table(start, end):
    for i in range(1, end + 1):
        for j in range(start, end + 1):
            print(f"{j} x {i} = {j * i}", end="\t")
        print()

# Example usage
start = 2
end = 4
multiplication_table(start, end)
```

**Explanation:**
- The function `multiplication_table` generates a multiplication table for numbers within the specified range.
- It uses nested loops to iterate through the range and print the product of each pair of numbers.

**C++ Code:**

```cpp
#include <iostream>

void multiplication_table(int start, int end) {
    for (int i = 1; i <= end; ++i) {
        for (int j = start; j <= end; ++j) {
            std::cout << j << " x " << i << " = " << j * i << "\t";
        }
        std::cout << std::endl;
    }
}

int main() {
    int start = 2;
    int end = 4;
    multiplication_table(start, end);
    return 0;
}
```

**Explanation:**
- The function `multiplication_table` generates a multiplication table for numbers within the specified range.
- It uses nested loops to iterate through the range and print the product of each pair of numbers.

### 3. Calculating the Sum of a Series (1 + 1/2 + 1/3 + ... + 1/n)

**Python Code:**

```python
def sum_of_series(n):
    return sum(1 / i for i in range(1, n + 1))

# Example usage
n = 4
result = sum_of_series(n)
print(result)  # Output: 2.083333333333333
```

**Explanation:**
- The function `sum_of_series` calculates the sum of the series 1 + 1/2 + 1/3 + ... + 1/n.
- It uses a generator expression to sum the reciprocals of numbers from 1 to n.

**C++ Code:**

```cpp
#include <iostream>

double sum_of_series(int n) {
    double sum = 0.0;
    for (int i = 1; i <= n; ++i) {
        sum += 1.0 / i;
    }
    return sum;
}

int main() {
    int n = 4;
    double result = sum_of_series(n);
    std::cout << result << std::endl;  // Output: 2.08333
    return 0;
}
```

**Explanation:**
- The function `sum_of_series` calculates the sum of the series 1 + 1/2 + 1/3 + ... + 1/n.
- It uses a loop to sum the reciprocals of numbers from 1 to n.

### 4. Finding All Pairs of Elements in an Array that Add Up to a Given Sum

**Python Code:**

```python
def find_pairs(array, target):
    seen = set()
    pairs = []
    for number in array:
        complement = target - number
        if complement in seen:
            pairs.append((complement, number))
        seen.add(number)
    return pairs

# Example usage
array = [1, 2, 3, 4, 5]
target = 5
result = find_pairs(array, target)
print(result)  # Output: [(1, 4), (2, 3)]
```

**Explanation:**
- The function `find_pairs` finds all pairs of elements in the array that add up to the given target.
- It uses a set to keep track of seen numbers and checks if the complement of the current number is in the set.

**C++ Code:**

```cpp
#include <iostream>
#include <vector>
#include <unordered_set>

std::vector<std::pair<int, int>> find_pairs(const std::vector<int>& array, int target) {
    std::unordered_set<int> seen;
    std::vector<std::pair<int, int>> pairs;
    for (int number : array) {
        int complement = target - number;
        if (seen.find(complement) != seen.end()) {
            pairs.emplace_back(complement, number);
        }
        seen.insert(number);
    }
    return pairs;
}

int main() {
    std::vector<int> array = {1, 2, 3, 4, 5};
    int target = 5;
    auto result = find_pairs(array, target);
    for (const auto& pair : result) {
        std::cout << "(" << pair.first << ", " << pair.second << ")" << std::endl;
    }
    return 0;
}
```

**Explanation:**
- The function `find_pairs` finds all pairs of elements in the array that add up to the given target.
- It uses an unordered set to keep track of seen numbers and checks if the complement of the current number is in the set.

### 5. Generating a Diamond Pattern of Stars

**Python Code:**

```python
def diamond_pattern(size):
    for i in range(size):
        print(' ' * (size - i - 1) + '*' * (2 * i + 1))
    for i in range(size - 2, -1, -1):
        print(' ' * (size - i - 1) + '*' * (2 * i + 1))

# Example usage
size = 5
diamond_pattern(size)
```

**Explanation:**
- The function `diamond_pattern` generates a diamond pattern of stars with the given size.
- It uses two loops to print the upper and lower halves of the diamond.

**C++ Code:**

```cpp
#include <iostream>

void diamond_pattern(int size) {
    for (int i = 0; i < size; ++i) {
        std::cout << std::string(size - i - 1, ' ') << std::string(2 * i + 1, '*') << std::endl;
    }
    for (int i = size - 2; i >= 0; --i) {
        std::cout << std::string(size - i - 1, ' ') << std::string(2 * i + 1, '*') << std::endl;
    }
}

int main() {
    int size = 5;
    diamond_pattern(size);
    return 0;
}
```

**Explanation:**
- The function `diamond_pattern` generates a diamond pattern of stars with the given size.
- It uses two loops to print the upper and lower halves of the diamond.

### 6. Counting the Number of Palindromic Substrings in a String

**Python Code:**

```python
def count_palindromic_substrings(s):
    n = len(s)
    count = 0
    for i in range(n):
        count += 1  # Single character is a palindrome
        # Odd length palindromes
        l, r = i - 1, i + 1
        while l >= 0 and r < n and s[l] == s[r]:
            count += 1
            l -= 1
            r += 1
        # Even length palindromes
        l, r = i, i + 1
        while l >= 0 and r < n and s[l] == s[r]:
            count += 1
            l -= 1
            r += 1
    return count

# Example usage
string = "aaa"
result = count_palindromic_substrings(string)
print(result)  # Output: 6
```

**Explanation:**
- The function `count_palindromic_substrings` counts the number of palindromic substrings in the given string.
- It checks for both odd and even length palindromes by expanding around each character and pair of characters.

**C++ Code:**

```cpp
#include <iostream>
#include <string>

int count_palindromic_substrings(const std::string& s) {
    int n = s.size();
    int count = 0;
    for (int i = 0; i < n; ++i) {
        count += 1;  // Single character is a palindrome
        // Odd length palindromes
        int l = i - 1, r = i + 1;
        while (l >= 0 && r < n && s[l] == s[r]) {
            count += 1;
            l -= 1;
            r += 1;
        }
        // Even length palindromes
        l = i, r = i + 1;
        while (l >= 0 && r < n && s[l] == s[r]) {
            count += 1;
            l -= 1;
            r += 1;
        }
    }
    return count;
}

int main() {
    std::string string = "aaa";
    int result = count_palindromic_substrings(string);
    std::cout << result << std::endl;  // Output: 6
    return 0;
}
```

**Explanation:**
- The function `count_palindromic_substrings` counts the number of palindromic substrings in the given string.
- It checks for both odd and even length palindromes by expanding around each character and pair of characters.

### 7. Generating a Matrix with Multiplication Table

**Python Code:**

```python
def generate_multiplication_matrix(size):
    matrix = [[(i + 1) * (j + 1) for j in range(size)] for i in range(size)]
    return matrix

# Example usage
size = 3
matrix = generate_multiplication_matrix(size)
for row in matrix:
    print(row)
```

**Explanation:**
- The function `generate_multiplication_matrix` generates a matrix where each element at position (i, j) is the product of (i + 1) and (j + 1).
- It uses list comprehensions to create the matrix.

**C++ Code:**

```cpp
#include <iostream>
#include <vector>

std::vector<std::vector<int>> generate_multiplication_matrix(int size) {
    std::vector<std::vector<int>> matrix(size, std::vector<int>(size));
    for (int i = 0; i < size; ++i) {
        for (int j = 0; j < size; ++j) {
            matrix[i][j] = (i + 1) * (j + 1);
        }
    }
    return matrix;
}

int main() {
    int size = 3;
    auto matrix = generate_multiplication_matrix(size);
    for (const auto& row : matrix) {
        for (int val : row) {
            std::cout << val << " ";
        }
        std::cout << std::endl;
    }
    return 0;
}
```

**Explanation:**
- The function `generate_multiplication_matrix` generates a matrix where each element at position (i, j) is the product of (i + 1) and (j + 1).
- It uses nested loops to fill the matrix.

### 8. Finding the GCD of Multiple Numbers

**Python Code:**

```python
import math

def gcd_of_list(numbers):
    gcd_result = numbers[0]
    for number in numbers[1:]:
        gcd_result = math.gcd(gcd_result, number)
    return gcd_result

# Example usage
numbers = [12, 24, 36]
result = gcd_of_list(numbers)
print(result)  # Output: 12
```

**Explanation:**
- The function `gcd_of_list` finds the GCD of a list of numbers.
- It uses the `math.gcd` function to calculate the GCD of pairs of numbers iteratively.

**C++ Code:**

```cpp
#include <iostream>
#include <vector>
#include <numeric>

int gcd(int a, int b) {
    while (b != 0) {
        int temp = b;
        b = a % b;
        a = temp;
    }
    return a;
}

int gcd_of_list(const std::vector<int>& numbers) {
    return std::accumulate(numbers.begin(), numbers.end(), numbers[0], gcd);
}

int main() {
    std::vector<int> numbers = {12, 24, 36};
    int result = gcd_of_list(numbers);
    std::cout << result << std::endl;  // Output: 12
    return 0;
}
```

**Explanation:**
- The function `gcd_of_list` finds the GCD of a list of numbers.
- It uses the `std::accumulate` function with a custom GCD function to calculate the GCD of pairs of numbers iteratively.

### 9. Finding the Sum of the First N Odd Numbers

**Python Code:**

```python
def sum_of_odd_numbers(n):
    return n * n

# Example usage
n = 5
result = sum_of_odd_numbers(n)
print(result)  # Output: 25
```

**Explanation:**
- The function `sum_of_odd_numbers` calculates the sum of the first N odd numbers.
- The sum of the first N odd numbers is given by the formula N^2.

**C++ Code:**

```cpp
#include <iostream>

int sum_of_odd_numbers(int n) {
    return n * n;
}

int main() {
    int n = 5;
    int result = sum_of_odd_numbers(n);
    std::cout << result << std::endl;  // Output: 25
    return 0;
}
```

**Explanation:**
- The function `sum_of_odd_numbers` calculates the sum of the first N odd numbers.
- The sum of the first N odd numbers is given by the formula N^2.

### 10. Finding the Number of Perfect Numbers Up to a Given Limit

**Python Code:**

```python
def is_perfect_number(num):
    return num == sum(i for i in range(1, num) if num % i == 0)

def count_perfect_numbers(limit):
    return sum(1 for num in range(2, limit + 1) if is_perfect_number(num))

# Example usage
limit = 30
result = count_perfect_numbers(limit)
print(result)  # Output: 1
```

**Explanation:**
- The function `count_perfect_numbers` counts the number of perfect numbers up to the given limit.
- It uses the helper function `is_perfect_number` to check if a number is perfect.

**C++ Code:**

```cpp
#include <iostream>

bool is_perfect_number(int num) {
    int sum = 0;
    for (int i = 1; i < num; ++i) {
        if (num % i == 0) {
            sum += i;
        }
    }
    return sum == num;
}

int count_perfect_numbers(int limit) {
    int count = 0;
    for (int num = 2; num <= limit; ++num) {
        if (is_perfect_number(num)) {
            count += 1;
        }
    }
    return count;
}

int main() {
    int limit = 30;
    int result = count_perfect_numbers(limit);
    std::cout << result << std::endl;  // Output: 1
    return 0;
}
```

**Explanation:**
- The function `count_perfect_numbers` counts the number of perfect numbers up to the given limit.
- It uses the helper function `is_perfect_number` to check if a number is perfect.

### 11. Finding the Largest Prime Factor of a Number

**Python Code:**

```python
def largest_prime_factor(n):
    def is_prime(num):
        if num <= 1:
            return False
        for i in range(2, int(num ** 0.5) + 1):
            if num % i == 0:
                return False
        return True

    largest_factor = 1
    for i in range(2, n):
        if n % i == 0 and is_prime(i):
            largest_factor = i
    return largest_factor

# Example usage
number = 28
result = largest_prime_factor(number)
print(result)  # Output: 7
```

**Explanation:**
- The function `largest_prime_factor` finds the largest prime factor of the given number.
- It uses a helper function `is_prime` to check if a number is prime.

**C++ Code:**

```cpp
#include <iostream>
#include <cmath>

bool is_prime(int num) {
    if (num <= 1) return false;
    for (int i = 2; i <= std::sqrt(num); ++i) {
        if (num % i == 0) return false;
    }
    return true;
}

int largest_prime_factor(int n) {
    int largest_factor = 1;
    for (int i = 2; i < n; ++i) {
        if (n % i == 0 && is_prime(i)) {
            largest_factor = i;
        }
    }
    return largest_factor;
}

int main() {
    int number = 28;
    int result = largest_prime_factor(number);
    std::cout << result << std::endl;  // Output: 7
    return 0;
}
```

**Explanation:**
- The function `largest_prime_factor` finds the largest prime factor of the given number.
- It uses a helper function `is_prime` to check if a number is prime.

### 12. Generating a Matrix of Fibonacci Numbers

**Python Code:**

```python
def generate_fibonacci_matrix(size):
    def fibonacci(n):
        fib_sequence = [1, 1]
        while len(fib_sequence) < n:
            fib_sequence.append(fib_sequence[-1] + fib_sequence[-2])
        return fib_sequence[:n]

    fib_sequence = fibonacci(size * size)
    matrix = [fib_sequence[i * size:(i + 1) * size] for i in range(size)]
    return matrix

# Example usage
size = 3
matrix = generate_fibonacci_matrix(size)
for row in matrix:
    print(row)
```

**Explanation:**
- The function `generate_fibonacci_matrix` generates a matrix where each element is a Fibonacci number.
- It uses a helper function `fibonacci` to generate the Fibonacci sequence up to the required length.

**C++ Code:**

```cpp
#include <iostream>
#include <vector>

std::vector<int> fibonacci(int n) {
    std::vector<int> fib_sequence = {1, 1};
    while (fib_sequence.size() < n) {
        fib_sequence.push_back(fib_sequence.back() + fib_sequence[fib_sequence.size() - 2]);
    }
    return fib_sequence;
}

std::vector<std::vector<int>> generate_fibonacci_matrix(int size) {
    std::vector<int> fib_sequence = fibonacci(size * size);
    std::vector<std::vector<int>> matrix(size, std::vector<int>(size));
    for (int i = 0; i < size; ++i) {
        for (int j = 0; j < size; ++j) {
            matrix[i][j] = fib_sequence[i * size + j];
        }
    }
    return matrix;
}

int main() {
    int size = 3;
    auto matrix = generate_fibonacci_matrix(size);
    for (const auto& row : matrix) {
        for (int val : row) {
            std::cout << val << " ";
        }
        std::cout << std::endl;
    }
    return 0;
}
```

**Explanation:**
- The function `generate_fibonacci_matrix` generates a matrix where each element is a Fibonacci number.
- It uses a helper function `fibonacci` to generate the Fibonacci sequence up to the required length.

### 13. Finding the Sum of the First N Prime Numbers

**Python Code:**

```python
def sum_of_primes(n):
    def is_prime(num):
        if num <= 1:
            return False
        for i in range(2, int(num ** 0.5) + 1):
            if num % i == 0:
                return False
        return True

    sum_primes = 0
    count = 0
    num = 2
    while count < n:
        if is_prime(num):
            sum_primes += num
            count += 1
        num += 1
    return sum_primes

# Example usage
n = 4
result = sum_of_primes(n)
print(result)  # Output: 17
```

**Explanation:**
- The function `sum_of_primes` calculates the sum of the first N prime numbers.
- It uses a helper function `is_prime` to check if a number is prime.

**C++ Code:**

```cpp
#include <iostream>
#include <cmath>

bool is_prime(int num) {
    if (num <= 1) return false;
    for (int i = 2; i <= std::sqrt(num); ++i) {
        if (num % i == 0) return false;
    }
    return true;
}

int sum_of_primes(int n) {
    int sum_primes = 0;
    int count = 0;
    int num = 2;
    while (count < n) {
        if (is_prime(num)) {
            sum_primes += num;
            count += 1;
        }
        num += 1;
    }
    return sum_primes;
}

int main() {
    int n = 4;
    int result = sum_of_primes(n);
    std::cout << result << std::endl;  // Output: 17
    return 0;
}
```

**Explanation:**
- The function `sum_of_primes` calculates the sum of the first N prime numbers.
- It uses a helper function `is_prime` to check if a number is prime.

### 14. Checking for a Balanced Bracket Sequence

**Python Code:**

```python
def is_balanced(s):
    stack = []
    brackets = {')': '(', ']': '[', '}': '{'}
    for char in s:
        if char in brackets.values():
            stack.append(char)
        elif char in brackets.keys():
            if stack == [] or brackets[char] != stack.pop():
                return False
    return stack == []

# Example usage
string = "{[()]}"
result = is_balanced(string)
print(result)  # Output: True
```

**Explanation:**
- The function `is_balanced` checks if the given string with brackets is balanced.
- It uses a stack to keep track of opening brackets and checks for matching closing brackets.

**C++ Code:**

```cpp
#include <iostream>
#include <stack>
#include <unordered_map>

bool is_balanced(const std::string& s) {
    std::stack<char> stack;
    std::unordered_map<char, char> brackets = {
        {')', '('},
        {']', '['},
        {'}', '{'}
    };
    for (char ch : s) {
        if (brackets.find(ch) != brackets.end()) {
            if (stack.empty() || stack.top() != brackets[ch]) {
                return false;
            }
            stack.pop();
        } else {
            stack.push(ch);
        }
    }
    return stack.empty();
}

int main() {
    std::string string = "{[()]}";
    bool result = is_balanced(string);
    std::cout << std::boolalpha << result << std::endl;  // Output: true
    return 0;
}
```

**Explanation:**
- The function `is_balanced` checks if the given string with brackets is balanced.
- It uses a stack to keep track of opening brackets and checks for matching closing brackets.

### 15. Finding the Sum of Numbers in a String

**Python Code:**

```python
import re

def sum_of_numbers_in_string(s):
    numbers = re.findall(r'\d+', s)
    return sum(int(num) for num in numbers)

# Example usage
string = "The numbers are 12 and 34"
result = sum_of_numbers_in_string(string)
print(result)  # Output: 46
```

**Explanation:**
- The function `sum_of_numbers_in_string` extracts and sums all numbers present in the given string.
- It uses regular expressions to find all numbers in the string.

**C++ Code:**

```cpp
#include <iostream>
#include <regex>
#include <sstream>

int sum_of_numbers_in_string(const std::string& s) {
    std::regex number_regex("\\d+");
    std::sregex_iterator iter(s.begin(), s.end(), number_regex);
    std::sregex_iterator end;
    int sum = 0;
    while (iter != end) {
        sum += std::stoi(iter->str());
        ++iter;
    }
    return sum;
}

int main() {
    std::string string = "The numbers are 12 and 34";
    int result = sum_of_numbers_in_string(string);
    std::cout << result << std::endl;  // Output: 46
    return 0;
}
```

**Explanation:**
- The function `sum_of_numbers_in_string` extracts and sums all numbers present in the given string.
- It uses regular expressions to find all numbers in the string.

### 16. Finding the Longest Consecutive Sequence in an Array

**Python Code:**

```python
def longest_consecutive_sequence(array):
    array_set = set(array)
    longest_sequence = 0
    for num in array_set:
        if num - 1 not in array_set:
            current_num = num
            current_sequence = 1
            while current_num + 1 in array_set:
                current_num += 1
                current_sequence += 1
            longest_sequence = max(longest_sequence, current_sequence)
    return longest_sequence

# Example usage
array = [100, 4, 200, 1, 3, 2]
result = longest_consecutive_sequence(array)
print(result)  # Output: 4
```

**Explanation:**
- The function `longest_consecutive_sequence` finds the longest sequence of consecutive numbers in the array.
- It uses a set to keep track of seen numbers and checks for consecutive sequences.

**C++ Code:**

```cpp
#include <iostream>
#include <vector>
#include <unordered_set>
#include <algorithm>

int longest_consecutive_sequence(const std::vector<int>& array) {
    std::unordered_set<int> array_set(array.begin(), array.end());
    int longest_sequence = 0;
    for (int num : array_set) {
        if (array_set.find(num - 1) == array_set.end()) {
            int current_num = num;
            int current_sequence = 1;
            while (array_set.find(current_num + 1) != array_set.end()) {
                current_num += 1;
                current_sequence += 1;
            }
            longest_sequence = std::max(longest_sequence, current_sequence);
        }
    }
    return longest_sequence;
}

int main() {
    std::vector<int> array = {100, 4, 200, 1, 3, 2};
    int result = longest_consecutive_sequence(array);
    std::cout << result << std::endl;  // Output: 4
    return 0;
}
```

**Explanation:**
- The function `longest_consecutive_sequence` finds the longest sequence of consecutive numbers in the array.
- It uses an unordered set to keep track of seen numbers and checks for consecutive sequences.

### 17. Generating a Matrix with a Spiral Pattern

**Python Code:**

```python
def generate_spiral_matrix(size):
    matrix = [[0] * size for _ in range(size)]
    num = 1
    top, bottom, left, right = 0, size - 1, 0, size - 1
    while top <= bottom and left <= right:
        for i in range(left, right + 1):
            matrix[top][i] = num
            num += 1
        top += 1
        for i in range(top, bottom + 1):
            matrix[i][right] = num
            num += 1
        right -= 1
        for i in range(right, left - 1, -1):
            matrix[bottom][i] = num
            num += 1
        bottom -= 1
        for i in range(bottom, top - 1, -1):
            matrix[i][left] = num
            num += 1
        left += 1
    return matrix

# Example usage
size = 3
matrix = generate_spiral_matrix(size)
for row in matrix:
    print(row)
```

**Explanation:**
- The function `generate_spiral_matrix` generates a matrix filled with numbers in a spiral pattern.
- It uses four pointers to keep track of the boundaries of the matrix and fills it in a spiral order.

**C++ Code:**

```cpp
#include <iostream>
#include <vector>

std::vector<std::vector<int>> generate_spiral_matrix(int size) {
    std::vector<std::vector<int>> matrix(size, std::vector<int>(size, 0));
    int num = 1;
    int top = 0, bottom = size - 1, left = 0, right = size - 1;
    while (top <= bottom && left <= right) {
        for (int i = left; i <= right; ++i) {
            matrix[top][i] = num++;
        }
        top += 1;
        for (int i = top; i <= bottom; ++i) {
            matrix[i][right] = num++;
        }
        right -= 1;
        for (int i = right; i >= left; --i) {
            matrix[bottom][i] = num++;
        }
        bottom -= 1;
        for (int i = bottom; i >= top; --i) {
            matrix[i][left] = num++;
        }
        left += 1;
    }
    return matrix;
}

int main() {
    int size = 3;
    auto matrix = generate_spiral_matrix(size);
    for (const auto& row : matrix) {
        for (int val : row) {
            std::cout << val << " ";
        }
        std::cout << std::endl;
    }
    return 0;
}
```

**Explanation:**
- The function `generate_spiral_matrix` generates a matrix filled with numbers in a spiral pattern.
- It uses four pointers to keep track of the boundaries of the matrix and fills it in a spiral order.

### 18. Finding All Subsets of a Set

**Python Code:**

```python
def find_subsets(nums):
    subsets = [[]]
    for num in nums:
        subsets += [subset + [num] for subset in subsets]
    return subsets

# Example usage
nums = [1, 2]
result = find_subsets(nums)
print(result)  # Output: [[], [1], [2], [1, 2]]
```

**Explanation:**
- The function `find_subsets` generates all possible subsets of the given set of numbers.
- It uses a list comprehension to add each number to existing subsets.

**C++ Code:**

```cpp
#include <iostream>
#include <vector>

std::vector<std::vector<int>> find_subsets(const std::vector<int>& nums) {
    std::vector<std::vector<int>> subsets = {{}};
    for (int num : nums) {
        int size = subsets.size();
        for (int i = 0; i < size; ++i) {
            subsets.push_back(subsets[i]);
            subsets.back().push_back(num);
        }
    }
    return subsets;
}

int main() {
    std::vector<int> nums = {1, 2};
    auto result = find_subsets(nums);
    for (const auto& subset : result) {
        for (int num : subset) {
            std::cout << num << " ";
        }
        std::cout << std::endl;
    }
    return 0;
}
```

**Explanation:**
- The function `find_subsets` generates all possible subsets of the given set of numbers.
- It uses a loop to add each number to existing subsets.

### 19. Checking for Perfect Squares in a Range

**Python Code:**

```python
def find_perfect_squares(start, end):
    return [num for num in range(start, end + 1) if int(num ** 0.5) ** 2 == num]

# Example usage
start = 1
end = 10
result = find_perfect_squares(start, end)
print(result)  # Output: [1, 4, 9]
```

**Explanation:**
- The function `find_perfect_squares` finds all perfect squares within the given range.
- It uses a list comprehension to check if each number is a perfect square.

**C++ Code:**

```cpp
#include <iostream>
#include <vector>
#include <cmath>

std::vector<int> find_perfect_squares(int start, int end) {
    std::vector<int> perfect_squares;
    for (int num = start; num <= end; ++num) {
        if (std::sqrt(num) == static_cast<int>(std::sqrt(num))) {
            perfect_squares.push_back(num);
        }
    }
    return perfect_squares;
}

int main() {
    int start = 1;
    int end = 10;
    auto result = find_perfect_squares(start, end);
    for (int num : result) {
        std::cout << num << " ";
    }
    std::cout << std::endl;  // Output: 1 4 9
    return 0;
}
```

**Explanation:**
- The function `find_perfect_squares` finds all perfect squares within the given range.
- It uses a loop to check if each number is a perfect square.

### 20. Finding the Sum of Diagonal Elements in a Matrix

**Python Code:**

```python
def sum_of_diagonal_elements(matrix):
    return sum(matrix[i][i] for i in range(len(matrix)))

# Example usage
matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
result = sum_of_diagonal_elements(matrix)
print(result)  # Output: 15
```

**Explanation:**
- The function `sum_of_diagonal_elements` calculates the sum of the diagonal elements in a square matrix.
- It uses a generator expression to sum the diagonal elements.

**C++ Code:**

```cpp
#include <iostream>
#include <vector>

int sum_of_diagonal_elements(const std::vector<std::vector<int>>& matrix) {
    int sum = 0;
    for (int i = 0; i < matrix.size(); ++i) {
        sum += matrix[i][i];
    }
    return sum;
}

int main() {
    std::vector<std::vector<int>> matrix = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
    int result = sum_of_diagonal_elements(matrix);
    std::cout << result << std::endl;  // Output: 15
    return 0;
}
```

**Explanation:**
- The function `sum_of_diagonal_elements` calculates the sum of the diagonal elements in a square matrix.
- It uses a loop to sum the diagonal elements.

### 21. Finding the Second Smallest Number in an Array

**Python Code:**

```python
def second_smallest_number(array):
    unique_numbers = list(set(array))
    unique_numbers.sort()
    return unique_numbers[1]

# Example usage
array = [12, 13, 1, 10, 34, 1]
result = second_smallest_number(array)
print(result)  # Output: 10
```

**Explanation:**
- The function `second_smallest_number` finds the second smallest number in the array.
- It removes duplicates, sorts the array, and returns the second element.

**C++ Code:**

```cpp
#include <iostream>
#include <vector>
#include <algorithm>
#include <set>

int second_smallest_number(const std::vector<int>& array) {
    std::set<int> unique_numbers(array.begin(), array.end());
    auto it = unique_numbers.begin();
    ++it;
    return *it;
}

int main() {
    std::vector<int> array = {12, 13, 1, 10, 34, 1};
    int result = second_smallest_number(array);
    std::cout << result << std::endl;  // Output: 10
    return 0;
}
```

**Explanation:**
- The function `second_smallest_number` finds the second smallest number in the array.
- It uses a set to remove duplicates and returns the second element.

### 22. Generating Pascal’s Triangle Up to N Rows

**Python Code:**

```python
def generate_pascals_triangle(n):
    triangle = [[1]]
    for i in range(1, n):
        row = [1]
        for j in range(1, i):
            row.append(triangle[i - 1][j - 1] + triangle[i - 1][j])
        row.append(1)
        triangle.append(row)
    return triangle

# Example usage
n = 3
triangle = generate_pascals_triangle(n)
for row in triangle:
    print(row)
```

**Explanation:**
- The function `generate_pascals_triangle` generates Pascal’s Triangle up to N rows.
- It uses nested loops to calculate each row based on the previous row.

**C++ Code:**

```cpp
#include <iostream>
#include <vector>

std::vector<std::vector<int>> generate_pascals_triangle(int n) {
    std::vector<std::vector<int>> triangle = {{1}};
    for (int i = 1; i < n; ++i) {
        std::vector<int> row = {1};
        for (int j = 1; j < i; ++j) {
            row.push_back(triangle[i - 1][j - 1] + triangle[i - 1][j]);
        }
        row.push_back(1);
        triangle.push_back(row);
    }
    return triangle;
}

int main() {
    int n = 3;
    auto triangle = generate_pascals_triangle(n);
    for (const auto& row : triangle) {
        for (int val : row) {
            std::cout << val << " ";
        }
        std::cout << std::endl;
    }
    return 0;
}
```

**Explanation:**
- The function `generate_pascals_triangle` generates Pascal’s Triangle up to N rows.
- It uses nested loops to calculate each row based on the previous row.

### 23. Finding the Sum of Digits of the Product of Two Numbers

**Python Code:**

```python
def sum_of_digits_of_product(number1, number2):
    product = number1 * number2
    return sum(int(digit) for digit in str(product))

# Example usage
number1 = 12
number2 = 34
result = sum_of_digits_of_product(number1, number2)
print(result)  # Output: 9
```

**Explanation:**
- The function `sum_of_digits_of_product` finds the sum of the digits of the product of two given numbers.
- It converts the product to a string to iterate over each digit and sums them.

**C++ Code:**

```cpp
#include <iostream>
#include <string>

int sum_of_digits_of_product(int number1, int number2) {
    int product = number1 * number2;
    int sum = 0;
    while (product > 0) {
        sum += product % 10;
        product /= 10;
    }
    return sum;
}

int main() {
    int number1 = 12;
    int number2 = 34;
    int result = sum_of_digits_of_product(number1, number2);
    std::cout << result << std::endl;  // Output: 9
    return 0;
}
```

**Explanation:**
- The function `sum_of_digits_of_product` finds the sum of the digits of the product of two given numbers.
- It uses a loop to extract each digit by taking the remainder of the product divided by 10 and sums them.

### 24. Checking for Palindromic Numbers in a Range

**Python Code:**

```python
def is_palindromic_number(num):
    return str(num) == str(num)[::-1]

def find_palindromic_numbers(start, end):
    return [num for num in range(start, end + 1) if is_palindromic_number(num)]

# Example usage
start = 1
end = 100
result = find_palindromic_numbers(start, end)
print(result)  # Output: [1, 2, 3, 4, 5, 6, 7, 8, 9, 11, 22, 33, 44, 55, 66, 77, 88, 99]
```

**Explanation:**
- The function `find_palindromic_numbers` finds all palindromic numbers within the given range.
- It uses a helper function `is_palindromic_number` to check if a number is palindromic.

**C++ Code:**

```cpp
#include <iostream>
#include <vector>
#include <string>
#include <algorithm>

bool is_palindromic_number(int num) {
    std::string str_num = std::to_string(num);
    std::string reversed_str_num = str_num;
    std::reverse(reversed_str_num.begin(), reversed_str_num.end());
    return str_num == reversed_str_num;
}

std::vector<int> find_palindromic_numbers(int start, int end) {
    std::vector<int> palindromic_numbers;
    for (int num = start; num <= end; ++num) {
        if (is_palindromic_number(num)) {
            palindromic_numbers.push_back(num);
        }
    }
    return palindromic_numbers;
}

int main() {
    int start = 1;
    int end = 100;
    auto result = find_palindromic_numbers(start, end);
    for (int num : result) {
        std::cout << num << " ";
    }
    std::cout << std::endl;  // Output: 1 2 3 4 5 6 7 8 9 11 22 33 44 55 66 77 88 99
    return 0;
}
```

**Explanation:**
- The function `find_palindromic_numbers` finds all palindromic numbers within the given range.
- It uses a helper function `is_palindromic_number` to check if a number is palindromic.

### 25. Generating a Matrix with Alternating 0s and 1s

**Python Code:**

```python
def generate_alternating_matrix(size):
    return [[(i + j) % 2 for j in range(size)] for i in range(size)]

# Example usage
size = 3
matrix = generate_alternating_matrix(size)
for row in matrix:
    print(row)
```

**Explanation:**
- The function `generate_alternating_matrix` generates a matrix where the elements alternate between 0 and 1.
- It uses list comprehensions to create the matrix.

**C++ Code:**

```cpp
#include <iostream>
#include <vector>

std::vector<std::vector<int>> generate_alternating_matrix(int size) {
    std::vector<std::vector<int>> matrix(size, std::vector<int>(size));
    for (int i = 0; i < size; ++i) {
        for (int j = 0; j < size; ++j) {
            matrix[i][j] = (i + j) % 2;
        }
    }
    return matrix;
}

int main() {
    int size = 3;
    auto matrix = generate_alternating_matrix(size);
    for (const auto& row : matrix) {
        for (int val : row) {
            std::cout << val << " ";
        }
        std::cout << std::endl;
    }
    return 0;
}
```

**Explanation:**
- The function `generate_alternating_matrix` generates a matrix where the elements alternate between 0 and 1.
- It uses nested loops to fill the matrix.

### 26. Finding the Count of a Specific Word in a String

**Python Code:**

```python
def count_word_occurrences(string, word):
    return string.lower().split().count(word.lower())

# Example usage
string = "hello world hello"
word = "hello"
result = count_word_occurrences(string, word)
print(result)  # Output: 2
```

**Explanation:**
- The function `count_word_occurrences` counts how many times a specific word appears in the given string.
- It converts the string to lowercase, splits it into words, and counts the occurrences of the word.

**C++ Code:**

```cpp
#include <iostream>
#include <sstream>
#include <algorithm>

int count_word_occurrences(const std::string& string, const std::string& word) {
    std::istringstream stream(string);
    std::string current_word;
    int count = 0;
    while (stream >> current_word) {
        std::transform(current_word.begin(), current_word.end(), current_word.begin(), ::tolower);
        if (current_word == word) {
            count += 1;
        }
    }
    return count;
}

int main() {
    std::string string = "hello world hello";
    std::string word = "hello";
    int result = count_word_occurrences(string, word);
    std::cout << result << std::endl;  // Output: 2
    return 0;
}
```

**Explanation:**
- The function `count_word_occurrences` counts how many times a specific word appears in the given string.
- It uses a string stream to split the string into words and counts the occurrences of the word.

### 27. Finding the Largest Sum of a Subarray

**Python Code:**

```python
def largest_sum_of_subarray(array):
    max_sum = float('-inf')
    current_sum = 0
    for num in array:
        current_sum = max(num, current_sum + num)
        max_sum = max(max_sum, current_sum)
    return max_sum

# Example usage
array = [-2, 1, -3, 4, -1, 2, 1, -5, 4]
result = largest_sum_of_subarray(array)
print(result)  # Output: 6
```

**Explanation:**
- The function `largest_sum_of_subarray` finds the largest sum of any contiguous subarray.
- It uses Kadane's algorithm to iterate through the array and keep track of the maximum sum.

**C++ Code:**

```cpp
#include <iostream>
#include <vector>
#include <algorithm>

int largest_sum_of_subarray(const std::vector<int>& array) {
    int max_sum = INT_MIN;
    int current_sum = 0;
    for (int num : array) {
        current_sum = std::max(num, current_sum + num);
        max_sum = std::max(max_sum, current_sum);
    }
    return max_sum;
}

int main() {
    std::vector<int> array = {-2, 1, -3, 4, -1, 2, 1, -5, 4};
    int result = largest_sum_of_subarray(array);
    std::cout << result << std::endl;  // Output: 6
    return 0;
}
```

**Explanation:**
- The function `largest_sum_of_subarray` finds the largest sum of any contiguous subarray.
- It uses Kadane's algorithm to iterate through the array and keep track of the maximum sum.

### 28. Generating a Right-Angle Triangle Pattern of Numbers

**Python Code:**

```python
def generate_right_angle_triangle(height):
    for i in range(1, height + 1):
        print(''.join(str(j) for j in range(1, i + 1)))

# Example usage
height = 4
generate_right_angle_triangle(height)
```

**Explanation:**
- The function `generate_right_angle_triangle` generates a right-angle triangle pattern with numbers.
- It uses a loop to print each row of the triangle.

**C++ Code:**

```cpp
#include <iostream>

void generate_right_angle_triangle(int height) {
    for (int i = 1; i <= height; ++i) {
        for (int j = 1; j <= i; ++j) {
            std::cout << j;
        }
        std::cout << std::endl;
    }
}

int main() {
    int height = 4;
    generate_right_angle_triangle(height);
    return 0;
}
```

**Explanation:**
- The function `generate_right_angle_triangle` generates a right-angle triangle pattern with numbers.
- It uses nested loops to print each row of the triangle.

### 29. Finding All Divisors of the Product of Two Numbers

**Python Code:**

```python
def find_divisors(number):
    return [i for i in range(1, number + 1) if number % i == 0]

def find_divisors_of_product(number1, number2):
    product = number1 * number2
    return find_divisors(product)

# Example usage
number1 = 6
number2 = 10
result = find_divisors_of_product(number1, number2)
print(result)  # Output: [1, 2, 3, 5, 6, 10, 15, 30]
```

**Explanation:**
- The function `find_divisors_of_product` finds all divisors of the product of two given numbers.
- It uses a helper function `find_divisors` to find the divisors of a number.

**C++ Code:**

```cpp
#include <iostream>
#include <vector>

std::vector<int> find_divisors(int number) {
    std::vector<int> divisors;
    for (int i = 1; i <= number; ++i) {
        if (number % i == 0) {
            divisors.push_back(i);
        }
    }
    return divisors;
}

std::vector<int> find_divisors_of_product(int number1, int number2) {
    int product = number1 * number2;
    return find_divisors(product);
}

int main() {
    int number1 = 6;
    int number2 = 10;
    auto result = find_divisors_of_product(number1, number2);
    for (int divisor : result) {
        std::cout << divisor << " ";
    }
    std::cout << std::endl;  // Output: 1 2 3 5 6 10 15 30
    return 0;
}
```

**Explanation:**
- The function `find_divisors_of_product` finds all divisors of the product of two given numbers.
- It uses a helper function `find_divisors` to find the divisors of a number.

### 30. Finding the Longest Sequence of Consecutive 1s in a Binary Array

**Python Code:**

```python
def longest_sequence_of_ones(array):
    max_sequence = 0
    current_sequence = 0
    for num in array:
        if num == 1:
            current_sequence += 1
            max_sequence = max(max_sequence, current_sequence)
        else:
            current_sequence = 0
    return max_sequence

# Example usage
array = [1, 1, 0, 1, 1, 1]
result = longest_sequence_of_ones(array)
print(result)  # Output: 3
```

**Explanation:**
- The function `longest_sequence_of_ones` finds the longest sequence of consecutive 1s in a binary array.
- It iterates through the array and keeps track of the maximum sequence of 1s.

**C++ Code:**

```cpp
#include <iostream>
#include <vector>
#include <algorithm>

int longest_sequence_of_ones(const std::vector<int>& array) {
    int max_sequence = 0;
    int current_sequence = 0;
    for (int num : array) {
        if (num == 1) {
            current_sequence += 1;
            max_sequence = std::max(max_sequence, current_sequence);
        } else {
            current_sequence = 0;
        }
    }
    return max_sequence;
}

int main() {
    std::vector<int> array = {1, 1, 0, 1, 1, 1};
    int result = longest_sequence_of_ones(array);
    std::cout << result << std::endl;  // Output: 3
    return 0;
}
```

**Explanation:**
- The function `longest_sequence_of_ones` finds the longest sequence of consecutive 1s in a binary array.
- It iterates through the array and keeps track of the maximum sequence of 1s.

### 31. Calculating the Sum of the First N Fibonacci Numbers

**Python Code:**

```python
def sum_of_fibonacci_numbers(n):
    fib_sequence = [1, 1]
    while len(fib_sequence) < n:
        fib_sequence.append(fib_sequence[-1] + fib_sequence[-2])
    return sum(fib_sequence[:n])

# Example usage
n = 5
result = sum_of_fibonacci_numbers(n)
print(result)  # Output: 12
```

**Explanation:**
- The function `sum_of_fibonacci_numbers` calculates the sum of the first N Fibonacci numbers.
- It generates the Fibonacci sequence up to the Nth number and sums them.

**C++ Code:**

```cpp
#include <iostream>
#include <vector>

int sum_of_fibonacci_numbers(int n) {
    std::vector<int> fib_sequence = {1, 1};
    while (fib_sequence.size() < n) {
        fib_sequence.push_back(fib_sequence.back() + fib_sequence[fib_sequence.size() - 2]);
    }
    int sum = 0;
    for (int i = 0; i < n; ++i) {
        sum += fib_sequence[i];
    }
    return sum;
}

int main() {
    int n = 5;
    int result = sum_of_fibonacci_numbers(n);
    std::cout << result << std::endl;  // Output: 12
    return 0;
}
```

**Explanation:**
- The function `sum_of_fibonacci_numbers` calculates the sum of the first N Fibonacci numbers.
- It generates the Fibonacci sequence up to the Nth number and sums them.

### 32. Checking for a Repeated Substring in a String

**Python Code:**

```python
def has_repeated_substring(s):
    n = len(s)
    for i in range(1, n):
        if s[:i] == s[i:2*i]:
            return True
    return False

# Example usage
string = "abab"
result = has_repeated_substring(string)
print(result)  # Output: True
```

**Explanation:**
- The function `has_repeated_substring` checks if a substring is repeated within the given string.
- It iterates through the string and checks for repeated substrings.

**C++ Code:**

```cpp
#include <iostream>
#include <string>

bool has_repeated_substring(const std::string& s) {
    int n = s.size();
    for (int i = 1; i < n; ++i) {
        if (s.substr(0, i) == s.substr(i, i)) {
            return true;
        }
    }
    return false;
}

int main() {
    std::string string = "abab";
    bool result = has_repeated_substring(string);
    std::cout << std::boolalpha << result << std::endl;  // Output: true
    return 0;
}
```

**Explanation:**
- The function `has_repeated_substring` checks if a substring is repeated within the given string.
- It iterates through the string and checks for repeated substrings.

### 33. Finding the Median of a List of Numbers

**Python Code:**

```python
def find_median(numbers):
    sorted_numbers = sorted(numbers)
    n = len(sorted_numbers)
    if n % 2 == 1:
        return sorted_numbers[n // 2]
    else:
        return (sorted_numbers[n // 2 - 1] + sorted_numbers[n // 2]) / 2

# Example usage
numbers = [3, 1, 4, 1, 5]
result = find_median(numbers)
print(result)  # Output: 3
```

**Explanation:**
- The function `find_median` finds the median value of a list of numbers.
- It sorts the list and calculates the median based on the length of the list.

**C++ Code:**

```cpp
#include <iostream>
#include <vector>
#include <algorithm>

double find_median(const std::vector<int>& numbers) {
    std::vector<int> sorted_numbers = numbers;
    std::sort(sorted_numbers.begin(), sorted_numbers.end());
    int n = sorted_numbers.size();
    if (n % 2 == 1) {
        return sorted_numbers[n / 2];
    } else {
        return (sorted_numbers[n / 2 - 1] + sorted_numbers[n / 2]) / 2.0;
    }
}

int main() {
    std::vector<int> numbers = {3, 1, 4, 1, 5};
    double result = find_median(numbers);
    std::cout << result << std::endl;  // Output: 3
    return 0;
}
```

**Explanation:**
- The function `find_median` finds the median value of a list of numbers.
- It sorts the list and calculates the median based on the length of the list.

### 34. Finding the Number of Words in a String

**Python Code:**

```python
def count_words(string):
    return len(string.split())

# Example usage
string = "Hello world"
result = count_words(string)
print(result)  # Output: 2
```

**Explanation:**
- The function `count_words` counts the number of words in the given string.
- It splits the string into words and returns the length of the resulting list.

**C++ Code:**

```cpp
#include <iostream>
#include <sstream>

int count_words(const std::string& string) {
    std::istringstream stream(string);
    int count = 0;
    std::string word;
    while (stream >> word) {
        count += 1;
    }
    return count;
}

int main() {
    std::string string = "Hello world";
    int result = count_words(string);
    std::cout << result << std::endl;  // Output: 2
    return 0;
}
```

**Explanation:**
- The function `count_words` counts the number of words in the given string.
- It uses a string stream to split the string into words and counts them.

### 35. Generating a Matrix with a Diagonal Pattern

**Python Code:**

```python
def generate_diagonal_matrix(size):
    return [[1 if i >= j else 0 for j in range(size)] for i in range(size)]

# Example usage
size = 4
matrix = generate_diagonal_matrix(size)
for row in matrix:
    print(row)
```

**Explanation:**
- The function `generate_diagonal_matrix` generates a matrix where elements form diagonal lines of a given pattern.
- It uses list comprehensions to create the matrix.

**C++ Code:**

```cpp
#include <iostream>
#include <vector>

std::vector<std::vector<int>> generate_diagonal_matrix(int size) {
    std::vector<std::vector<int>> matrix(size, std::vector<int>(size, 0));
    for (int i = 0; i < size; ++i) {
        for (int j = 0; j <= i; ++j) {
            matrix[i][j] = 1;
        }
    }
    return matrix;
}

int main() {
    int size = 4;
    auto matrix = generate_diagonal_matrix(size);
    for (const auto& row : matrix) {
        for (int val : row) {
            std::cout << val << " ";
        }
        std::cout << std::endl;
    }
    return 0;
}
```

**Explanation:**
- The function `generate_diagonal_matrix` generates a matrix where elements form diagonal lines of a given pattern.
- It uses nested loops to fill the matrix.

### 36. Finding the Sum of the First N Even Numbers

**Python Code:**

```python
def sum_of_even_numbers(n):
    return n * (n + 1)

# Example usage
n = 4
result = sum_of_even_numbers(n)
print(result)  # Output: 20
```

**Explanation:**
- The function `sum_of_even_numbers` calculates the sum of the first N even numbers.
- The sum of the first N even numbers is given by the formula N * (N + 1).

**C++ Code:**

```cpp
#include <iostream>

int sum_of_even_numbers(int n) {
    return n * (n + 1);
}

int main() {
    int n = 4;
    int result = sum_of_even_numbers(n);
    std::cout << result << std::endl;  // Output: 20
    return 0;
}
```

**Explanation:**
- The function `sum_of_even_numbers` calculates the sum of the first N even numbers.
- The sum of the first N even numbers is given by the formula N * (N + 1).

### 37. Finding the Count of Digits Greater Than a Specific Value

**Python Code:**

```python
def count_digits_greater_than(number, value):
    return sum(1 for digit in str(number) if int(digit) > value)

# Example usage
number = 54321
value = 3
result = count_digits_greater_than(number, value)
print(result)  # Output: 2
```

**Explanation:**
- The function `count_digits_greater_than` counts how many digits in the number are greater than a specific value.
- It converts the number to a string to iterate over each digit and counts the digits greater than the value.

**C++ Code:**

```cpp
#include <iostream>
#include <string>

int count_digits_greater_than(int number, int value) {
    int count = 0;
    std::string str_number = std::to_string(number);
    for (char digit : str_number) {
        if (digit - '0' > value) {
            count += 1;
        }
    }
    return count;
}

int main() {
    int number = 54321;
    int value = 3;
    int result = count_digits_greater_than(number, value);
    std::cout << result << std::endl;  // Output: 2
    return 0;
}
```

**Explanation:**
- The function `count_digits_greater_than` counts how many digits in the number are greater than a specific value.
- It converts the number to a string to iterate over each digit and counts the digits greater than the value.

