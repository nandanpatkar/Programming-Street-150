Let's go through each of the questions, providing both Python and C++ code solutions along with explanations.

### 1. Determining Even/Odd Numbers

**Python Code:**
```python
def check_even_odd(number):
    if number % 2 == 0:
        return "Even"
    else:
        return "Odd"

# Example usage
number = 4
print(check_even_odd(number))  # Output: Even
```
**Explanation:** The function `check_even_odd` checks if a number is divisible by 2. If it is, the number is even; otherwise, it is odd.

**C++ Code:**
```cpp
#include <iostream>
using namespace std;

string checkEvenOdd(int number) {
    if (number % 2 == 0) {
        return "Even";
    } else {
        return "Odd";
    }
}

int main() {
    int number = 4;
    cout << checkEvenOdd(number) << endl;  // Output: Even
    return 0;
}
```
**Explanation:** The function `checkEvenOdd` performs the same check as the Python version, using the modulus operator to determine if the number is even or odd.

### 2. Checking for Prime Numbers

**Python Code:**
```python
def is_prime(number):
    if number <= 1:
        return "Not Prime"
    for i in range(2, int(number ** 0.5) + 1):
        if number % i == 0:
            return "Not Prime"
    return "Prime"

# Example usage
number = 7
print(is_prime(number))  # Output: Prime
```
**Explanation:** The function `is_prime` checks if a number is prime by testing divisibility from 2 up to the square root of the number.

**C++ Code:**
```cpp
#include <iostream>
#include <cmath>
using namespace std;

string isPrime(int number) {
    if (number <= 1) {
        return "Not Prime";
    }
    for (int i = 2; i <= sqrt(number); ++i) {
        if (number % i == 0) {
            return "Not Prime";
        }
    }
    return "Prime";
}

int main() {
    int number = 7;
    cout << isPrime(number) << endl;  // Output: Prime
    return 0;
}
```
**Explanation:** The function `isPrime` follows the same logic as the Python version, using a loop to check for factors up to the square root of the number.

### 3. Validating Leap Years

**Python Code:**
```python
def is_leap_year(year):
    if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
        return "Leap Year"
    else:
        return "Not Leap Year"

# Example usage
year = 2020
print(is_leap_year(year))  # Output: Leap Year
```
**Explanation:** The function `is_leap_year` checks if a year is a leap year by applying the rules for leap years.

**C++ Code:**
```cpp
#include <iostream>
using namespace std;

string isLeapYear(int year) {
    if ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0)) {
        return "Leap Year";
    } else {
        return "Not Leap Year";
    }
}

int main() {
    int year = 2020;
    cout << isLeapYear(year) << endl;  // Output: Leap Year
    return 0;
}
```
**Explanation:** The function `isLeapYear` uses the same logic as the Python version to determine if a year is a leap year.

### 4. Calculating Armstrong Numbers

**Python Code:**
```python
def is_armstrong_number(number):
    digits = [int(d) for d in str(number)]
    power = len(digits)
    armstrong_sum = sum(d ** power for d in digits)
    return "Armstrong Number" if armstrong_sum == number else "Not Armstrong Number"

# Example usage
number = 153
print(is_armstrong_number(number))  # Output: Armstrong Number
```
**Explanation:** The function `is_armstrong_number` calculates the sum of the digits raised to the power of the number of digits and checks if it equals the original number.

**C++ Code:**
```cpp
#include <iostream>
#include <cmath>
using namespace std;

string isArmstrongNumber(int number) {
    int originalNumber = number;
    int sum = 0;
    int digits = 0;

    // Count the number of digits
    int temp = number;
    while (temp > 0) {
        digits++;
        temp /= 10;
    }

    // Calculate the Armstrong sum
    temp = number;
    while (temp > 0) {
        int digit = temp % 10;
        sum += pow(digit, digits);
        temp /= 10;
    }

    return (sum == originalNumber) ? "Armstrong Number" : "Not Armstrong Number";
}

int main() {
    int number = 153;
    cout << isArmstrongNumber(number) << endl;  // Output: Armstrong Number
    return 0;
}
```
**Explanation:** The function `isArmstrongNumber` follows the same logic as the Python version, using loops to count digits and calculate the Armstrong sum.

### 5. Generating the Fibonacci Series

**Python Code:**
```python
def fibonacci_series(limit):
    series = [0, 1]
    while True:
        next_value = series[-1] + series[-2]
        if next_value > limit:
            break
        series.append(next_value)
    return series

# Example usage
limit = 10
print(fibonacci_series(limit))  # Output: [0, 1, 1, 2, 3, 5, 8]
```
**Explanation:** The function `fibonacci_series` generates the Fibonacci series up to a given limit by iteratively adding the last two numbers in the series.

**C++ Code:**
```cpp
#include <iostream>
#include <vector>
using namespace std;

vector<int> fibonacciSeries(int limit) {
    vector<int> series = {0, 1};
    while (true) {
        int nextValue = series.back() + *(series.end() - 2);
        if (nextValue > limit) {
            break;
        }
        series.push_back(nextValue);
    }
    return series;
}

int main() {
    int limit = 10;
    vector<int> series = fibonacciSeries(limit);
    for (int num : series) {
        cout << num << " ";
    }
    cout << endl;  // Output: 0 1 1 2 3 5 8
    return 0;
}
```
**Explanation:** The function `fibonacciSeries` uses a vector to store the Fibonacci series and a loop to generate the series up to the given limit.

### 6. Identifying Palindromes

**Python Code:**
```python
def is_palindrome(string):
    return "Palindrome" if string == string[::-1] else "Not Palindrome"

# Example usage
string = "radar"
print(is_palindrome(string))  # Output: Palindrome
```
**Explanation:** The function `is_palindrome` checks if a string is equal to its reverse.

**C++ Code:**
```cpp
#include <iostream>
#include <algorithm>
using namespace std;

string isPalindrome(string str) {
    string reversedStr = str;
    reverse(reversedStr.begin(), reversedStr.end());
    return (str == reversedStr) ? "Palindrome" : "Not Palindrome";
}

int main() {
    string str = "radar";
    cout << isPalindrome(str) << endl;  // Output: Palindrome
    return 0;
}
```
**Explanation:** The function `isPalindrome` reverses the string and compares it to the original to check if it is a palindrome.

### 7. Crafting Star Patterns

**Python Code:**
```python
def print_pyramid(height):
    for i in range(1, height + 1):
        print(' ' * (height - i) + '*' * (2 * i - 1))

# Example usage
height = 5
print_pyramid(height)
```
**Explanation:** The function `print_pyramid` generates a pyramid pattern by printing spaces and asterisks in a loop.

**C++ Code:**
```cpp
#include <iostream>
using namespace std;

void printPyramid(int height) {
    for (int i = 1; i <= height; ++i) {
        cout << string(height - i, ' ') << string(2 * i - 1, '*') << endl;
    }
}

int main() {
    int height = 5;
    printPyramid(height);
    return 0;
}
```
**Explanation:** The function `printPyramid` follows the same logic as the Python version, using loops to print the pyramid pattern.

### 8. Finding the Factorial of a Number

**Python Code:**
```python
def factorial(number):
    if number == 0:
        return 1
    result = 1
    for i in range(1, number + 1):
        result *= i
    return result

# Example usage
number = 5
print(factorial(number))  # Output: 120
```
**Explanation:** The function `factorial` calculates the factorial of a number using a loop.

**C++ Code:**
```cpp
#include <iostream>
using namespace std;

int factorial(int number) {
    if (number == 0) {
        return 1;
    }
    int result = 1;
    for (int i = 1; i <= number; ++i) {
        result *= i;
    }
    return result;
}

int main() {
    int number = 5;
    cout << factorial(number) << endl;  // Output: 120
    return 0;
}
```
**Explanation:** The function `factorial` uses a loop to calculate the factorial of a number, similar to the Python version.

### 9. Summing Digits of a Number

**Python Code:**
```python
def sum_of_digits(number):
    return sum(int(digit) for digit in str(number))

# Example usage
number = 1234
print(sum_of_digits(number))  # Output: 10
```
**Explanation:** The function `sum_of_digits` converts the number to a string, iterates over each digit, converts it back to an integer, and sums them.

**C++ Code:**
```cpp
#include <iostream>
using namespace std;

int sumOfDigits(int number) {
    int sum = 0;
    while (number > 0) {
        sum += number % 10;
        number /= 10;
    }
    return sum;
}

int main() {
    int number = 1234;
    cout << sumOfDigits(number) << endl;  // Output: 10
    return 0;
}
```
**Explanation:** The function `sumOfDigits` uses a loop to extract each digit and sum them.

### 10. Finding the Greatest Common Divisor (GCD)

**Python Code:**
```python
def gcd(a, b):
    while b:
        a, b = b, a % b
    return a

# Example usage
a = 48
b = 18
print(gcd(a, b))  # Output: 6
```
**Explanation:** The function `gcd` uses the Euclidean algorithm to find the greatest common divisor of two numbers.

**C++ Code:**
```cpp
#include <iostream>
using namespace std;

int gcd(int a, int b) {
    while (b) {
        int temp = b;
        b = a % b;
        a = temp;
    }
    return a;
}

int main() {
    int a = 48;
    int b = 18;
    cout << gcd(a, b) << endl;  // Output: 6
    return 0;
}
```
**Explanation:** The function `gcd` follows the same logic as the Python version, using a loop to implement the Euclidean algorithm.

### 11. Finding the Least Common Multiple (LCM)

**Python Code:**
```python
def lcm(a, b):
    from math import gcd
    return a * b // gcd(a, b)

# Example usage
a = 12
b = 15
print(lcm(a, b))  # Output: 60
```
**Explanation:** The function `lcm` calculates the least common multiple using the formula involving the GCD.

**C++ Code:**
```cpp
#include <iostream>
#include <numeric>
using namespace std;

int lcm(int a, int b) {
    return a * b / gcd(a, b);
}

int main() {
    int a = 12;
    int b = 15;
    cout << lcm(a, b) << endl;  // Output: 60
    return 0;
}
```
**Explanation:** The function `lcm` uses the same formula as the Python version to calculate the LCM.

### 12. Counting Vowels and Consonants in a String

**Python Code:**
```python
def count_vowels_consonants(string):
    vowels = "aeiouAEIOU"
    vowel_count = consonant_count = 0
    for char in string:
        if char.isalpha():
            if char in vowels:
                vowel_count += 1
            else:
                consonant_count += 1
    return f"Vowels: {vowel_count}, Consonants: {consonant_count}"

# Example usage
string = "hello world"
print(count_vowels_consonants(string))  # Output: Vowels: 3, Consonants: 7
```
**Explanation:** The function `count_vowels_consonants` iterates over each character in the string, checking if it is a vowel or consonant and counting accordingly.

**C++ Code:**
```cpp
#include <iostream>
#include <cctype>
using namespace std;

string countVowelsConsonants(const string& str) {
    string vowels = "aeiouAEIOU";
    int vowelCount = 0, consonantCount = 0;
    for (char ch : str) {
        if (isalpha(ch)) {
            if (vowels.find(ch) != string::npos) {
                vowelCount++;
            } else {
                consonantCount++;
            }
        }
    }
    return "Vowels: " + to_string(vowelCount) + ", Consonants: " + to_string(consonantCount);
}

int main() {
    string str = "hello world";
    cout << countVowelsConsonants(str) << endl;  // Output: Vowels: 3, Consonants: 7
    return 0;
}
```
**Explanation:** The function `countVowelsConsonants` follows the same logic as the Python version, using loops and conditionals to count vowels and consonants.

### 13. Reversing a String

**Python Code:**
```python
def reverse_string(string):
    return string[::-1]

# Example usage
string = "programming"
print(reverse_string(string))  # Output: gnimmargorp
```
**Explanation:** The function `reverse_string` uses slicing to reverse the string.

**C++ Code:**
```cpp
#include <iostream>
#include <algorithm>
using namespace std;

string reverseString(string str) {
    reverse(str.begin(), str.end());
    return str;
}

int main() {
    string str = "programming";
    cout << reverseString(str) << endl;  // Output: gnimmargorp
    return 0;
}
```
**Explanation:** The function `reverseString` uses the `reverse` function from the algorithm library to reverse the string.

### 14. Finding the Largest and Smallest Numbers in an Array

**Python Code:**
```python
def find_largest_smallest(array):
    largest = max(array)
    smallest = min(array)
    return f"Largest: {largest}, Smallest: {smallest}"

# Example usage
array = [4, 7, 1, 8, 5]
print(find_largest_smallest(array))  # Output: Largest: 8, Smallest: 1
```
**Explanation:** The function `find_largest_smallest` uses the `max` and `min` functions to find the largest and smallest numbers in the array.

**C++ Code:**
```cpp
#include <iostream>
#include <vector>
#include <algorithm>
using namespace std;

string findLargestSmallest(const vector<int>& array) {
    int largest = *max_element(array.begin(), array.end());
    int smallest = *min_element(array.begin(), array.end());
    return "Largest: " + to_string(largest) + ", Smallest: " + to_string(smallest);
}

int main() {
    vector<int> array = {4, 7, 1, 8, 5};
    cout << findLargestSmallest(array) << endl;  // Output: Largest: 8, Smallest: 1
    return 0;
}
```
**Explanation:** The function `findLargestSmallest` uses the `max_element` and `min_element` functions to find the largest and smallest numbers in the array.

### 15. Sorting an Array

**Python Code:**
```python
def sort_array(array):
    return sorted(array)

# Example usage
array = [3, 1, 4, 1, 5, 9]
print(sort_array(array))  # Output: [1, 1, 3, 4, 5, 9]
```
**Explanation:** The function `sort_array` uses the `sorted` function to sort the array in ascending order.

**C++ Code:**
```cpp
#include <iostream>
#include <vector>
#include <algorithm>
using namespace std;

vector<int> sortArray(vector<int> array) {
    sort(array.begin(), array.end());
    return array;
}

int main() {
    vector<int> array = {3, 1, 4, 1, 5, 9};
    vector<int> sortedArray = sortArray(array);
    for (int num : sortedArray) {
        cout << num << " ";
    }
    cout << endl;  // Output: 1 1 3 4 5 9
    return 0;
}
```
**Explanation:** The function `sortArray` uses the `sort` function to sort the array in ascending order.

### 16. Finding the Sum of Elements in an Array

**Python Code:**
```python
def sum_of_elements(array):
    return sum(array)

# Example usage
array = [1, 2, 3, 4, 5]
print(sum_of_elements(array))  # Output: 15
```
**Explanation:** The function `sum_of_elements` uses the `sum` function to calculate the sum of elements in the array.

**C++ Code:**
```cpp
#include <iostream>
#include <vector>
#include <numeric>
using namespace std;

int sumOfElements(const vector<int>& array) {
    return accumulate(array.begin(), array.end(), 0);
}

int main() {
    vector<int> array = {1, 2, 3, 4, 5};
    cout << sumOfElements(array) << endl;  // Output: 15
    return 0;
}
```
**Explanation:** The function `sumOfElements` uses the `accumulate` function to calculate the sum of elements in the array.

### 17. Checking for Armstrong Numbers in a Range

**Python Code:**
```python
def find_armstrong_numbers(range_start, range_end):
    armstrong_numbers = []
    for number in range(range_start, range_end + 1):
        digits = [int(d) for d in str(number)]
        power = len(digits)
        if sum(d ** power for d in digits) == number:
            armstrong_numbers.append(number)
    return armstrong_numbers

# Example usage
range_start = 1
range_end = 500
print(find_armstrong_numbers(range_start, range_end))  # Output: [1, 153, 370, 371, 407]
```
**Explanation:** The function `find_armstrong_numbers` iterates through a range of numbers, checking each one to see if it is an Armstrong number.

**C++ Code:**
```cpp
#include <iostream>
#include <vector>
#include <cmath>
using namespace std;

vector<int> findArmstrongNumbers(int rangeStart, int rangeEnd) {
    vector<int> armstrongNumbers;
    for (int number = rangeStart; number <= rangeEnd; ++number) {
        int originalNumber = number;
        int sum = 0;
        int digits = 0;

        // Count the number of digits
        int temp = number;
        while (temp > 0) {
            digits++;
            temp /= 10;
        }

        // Calculate the Armstrong sum
        temp = number;
        while (temp > 0) {
            int digit = temp % 10;
            sum += pow(digit, digits);
            temp /= 10;
        }

        if (sum == originalNumber) {
            armstrongNumbers.push_back(number);
        }
    }
    return armstrongNumbers;
}

int main() {
    int rangeStart = 1;
    int rangeEnd = 500;
    vector<int> armstrongNumbers = findArmstrongNumbers(rangeStart, rangeEnd);
    for (int num : armstrongNumbers) {
        cout << num << " ";
    }
    cout << endl;  // Output: 1 153 370 371 407
    return 0;
}
```
**Explanation:** The function `findArmstrongNumbers` follows the same logic as the Python version, using loops to check each number in the range.

### 18. Generating Multiplication Tables

**Python Code:**
```python
def generate_multiplication_table(number, limit):
    for i in range(1, limit + 1):
        print(f"{number} x {i} = {number * i}")

# Example usage
number = 4
limit = 5
generate_multiplication_table(number, limit)
```
**Explanation:** The function `generate_multiplication_table` generates the multiplication table for a given number up to a specified limit.

**C++ Code:**
```cpp
#include <iostream>
using namespace std;

void generateMultiplicationTable(int number, int limit) {
    for (int i = 1; i <= limit; ++i) {
        cout << number << " x " << i << " = " << number * i << endl;
    }
}

int main() {
    int number = 4;
    int limit = 5;
    generateMultiplicationTable(number, limit);
    return 0;
}
```
**Explanation:** The function `generateMultiplicationTable` follows the same logic as the Python version, using a loop to generate the multiplication table.

### 19. Finding Prime Numbers in a Range

**Python Code:**
```python
def find_prime_numbers(range_start, range_end):
    prime_numbers = []
    for number in range(range_start, range_end + 1):
        if number > 1:
            is_prime = True
            for i in range(2, int(number ** 0.5) + 1):
                if number % i == 0:
                    is_prime = False
                    break
            if is_prime:
                prime_numbers.append(number)
    return prime_numbers

# Example usage
range_start = 10
range_end = 30
print(find_prime_numbers(range_start, range_end))  # Output: [11, 13, 17, 19, 23, 29]
```
**Explanation:** The function `find_prime_numbers` iterates through a range of numbers, checking each one to see if it is a prime number.

**C++ Code:**
```cpp
#include <iostream>
#include <vector>
#include <cmath>
using namespace std;

vector<int> findPrimeNumbers(int rangeStart, int rangeEnd) {
    vector<int> primeNumbers;
    for (int number = rangeStart; number <= rangeEnd; ++number) {
        if (number > 1) {
            bool isPrime = true;
            for (int i = 2; i <= sqrt(number); ++i) {
                if (number % i == 0) {
                    isPrime = false;
                    break;
                }
            }
            if (isPrime) {
                primeNumbers.push_back(number);
            }
        }
    }
    return primeNumbers;
}

int main() {
    int rangeStart = 10;
    int rangeEnd = 30;
    vector<int> primeNumbers = findPrimeNumbers(rangeStart, rangeEnd);
    for (int num : primeNumbers) {
        cout << num << " ";
    }
    cout << endl;  // Output: 11 13 17 19 23 29
    return 0;
}
```
**Explanation:** The function `findPrimeNumbers` follows the same logic as the Python version, using loops to check each number in the range.

### 20. Checking for Perfect Numbers

**Python Code:**
```python
def is_perfect_number(number):
    divisors = [i for i in range(1, number) if number % i == 0]
    return "Perfect Number" if sum(divisors) == number else "Not Perfect Number"

# Example usage
number = 28
print(is_perfect_number(number))  # Output: Perfect Number
```
**Explanation:** The function `is_perfect_number` finds all divisors of a number and checks if their sum equals the number.

**C++ Code:**
```cpp
#include <iostream>
#include <vector>
using namespace std;

string isPerfectNumber(int number) {
    vector<int> divisors;
    for (int i = 1; i < number; ++i) {
        if (number % i == 0) {
            divisors.push_back(i);
        }
    }
    int sum = 0;
    for (int divisor : divisors) {
        sum += divisor;
    }
    return (sum == number) ? "Perfect Number" : "Not Perfect Number";
}

int main() {
    int number = 28;
    cout << isPerfectNumber(number) << endl;  // Output: Perfect Number
    return 0;
}
```
**Explanation:** The function `isPerfectNumber` follows the same logic as the Python version, using loops to find divisors and sum them.

### 21. Calculating the Sum of Even Numbers in a Range

**Python Code:**
```python
def sum_of_even_numbers(range_start, range_end):
    return sum(number for number in range(range_start, range_end + 1) if number % 2 == 0)

# Example usage
range_start = 1
range_end = 10
print(sum_of_even_numbers(range_start, range_end))  # Output: 30
```
**Explanation:** The function `sum_of_even_numbers` uses a generator expression to sum all even numbers in a range.

**C++ Code:**
```cpp
#include <iostream>
using namespace std;

int sumOfEvenNumbers(int rangeStart, int rangeEnd) {
    int sum = 0;
    for (int number = rangeStart; number <= rangeEnd; ++number) {
        if (number % 2 == 0) {
            sum += number;
        }
    }
    return sum;
}

int main() {
    int rangeStart = 1;
    int rangeEnd = 10;
    cout << sumOfEvenNumbers(rangeStart, rangeEnd) << endl;  // Output: 30
    return 0;
}
```
**Explanation:** The function `sumOfEvenNumbers` uses a loop to sum all even numbers in a range.

### 22. Calculating the Sum of Odd Numbers in a Range

**Python Code:**
```python
def sum_of_odd_numbers(range_start, range_end):
    return sum(number for number in range(range_start, range_end + 1) if number % 2 != 0)

# Example usage
range_start = 1
range_end = 10
print(sum_of_odd_numbers(range_start, range_end))  # Output: 25
```
**Explanation:** The function `sum_of_odd_numbers` uses a generator expression to sum all odd numbers in a range.

**C++ Code:**
```cpp
#include <iostream>
using namespace std;

int sumOfOddNumbers(int rangeStart, int rangeEnd) {
    int sum = 0;
    for (int number = rangeStart; number <= rangeEnd; ++number) {
        if (number % 2 != 0) {
            sum += number;
        }
    }
    return sum;
}

int main() {
    int rangeStart = 1;
    int rangeEnd = 10;
    cout << sumOfOddNumbers(rangeStart, rangeEnd) << endl;  // Output: 25
    return 0;
}
```
**Explanation:** The function `sumOfOddNumbers` uses a loop to sum all odd numbers in a range.

### 23. Finding the Fibonacci Number at a Specific Position

**Python Code:**
```python
def fibonacci_at_position(position):
    a, b = 0, 1
    for _ in range(position):
        a, b = b, a + b
    return a

# Example usage
position = 5
print(fibonacci_at_position(position))  # Output: 5
```
**Explanation:** The function `fibonacci_at_position` iteratively calculates the Fibonacci number at a specific position.

**C++ Code:**
```cpp
#include <iostream>
using namespace std;

int fibonacciAtPosition(int position) {
    int a = 0, b = 1;
    for (int i = 0; i < position; ++i) {
        int temp = a;
        a = b;
        b = temp + b;
    }
    return a;
}

int main() {
    int position = 5;
    cout << fibonacciAtPosition(position) << endl;  // Output: 5
    return 0;
}
```
**Explanation:** The function `fibonacciAtPosition` follows the same logic as the Python version, using a loop to calculate the Fibonacci number at a specific position.

### 24. Printing Prime Numbers Less Than a Given Number

**Python Code:**
```python
def print_primes_less_than(number):
    primes = []
    for num in range(2, number):
        is_prime = True
        for i in range(2, int(num ** 0.5) + 1):
            if num % i == 0:
                is_prime = False
                break
        if is_prime:
            primes.append(num)
    return primes

# Example usage
number = 20
print(print_primes_less_than(number))  # Output: [2, 3, 5, 7, 11, 13, 17, 19]
```
**Explanation:** The function `print_primes_less_than` iterates through numbers less than a given number, checking each one to see if it is a prime number.

**C++ Code:**
```cpp
#include <iostream>
#include <vector>
#include <cmath>
using namespace std;

vector<int> printPrimesLessThan(int number) {
    vector<int> primes;
    for (int num = 2; num < number; ++num) {
        bool isPrime = true;
        for (int i = 2; i <= sqrt(num); ++i) {
            if (num % i == 0) {
                isPrime = false;
                break;
            }
        }
        if (isPrime) {
            primes.push_back(num);
        }
    }
    return primes;
}

int main() {
    int number = 20;
    vector<int> primes = printPrimesLessThan(number);
    for (int prime : primes) {
        cout << prime << " ";
    }
    cout << endl;  // Output: 2 3 5 7 11 13 17 19
    return 0;
}
```
**Explanation:** The function `printPrimesLessThan` follows the same logic as the Python version, using loops to check each number.

### 25. Finding the Number of Digits in a Number

**Python Code:**
```python
def count_digits(number):
    return len(str(number))

# Example usage
number = 12345
print(count_digits(number))  # Output: 5
```
**Explanation:** The function `count_digits` converts the number to a string and returns its length.

**C++ Code:**
```cpp
#include <iostream>
#include <cmath>
using namespace std;

int countDigits(int number) {
    return (number == 0) ? 1 : log10(abs(number)) + 1;
}

int main() {
    int number = 12345;
    cout << countDigits(number) << endl;  // Output: 5
    return 0;
}
```
**Explanation:** The function `countDigits` uses the logarithm to determine the number of digits in a number.

### 26. Checking if a Number is a Narcissistic Number

**Python Code:**
```python
def is_narcissistic_number(number):
    digits = [int(d) for d in str(number)]
    power = len(digits)
    return "Narcissistic Number" if sum(d ** power for d in digits) == number else "Not Narcissistic Number"

# Example usage
number = 153
print(is_narcissistic_number(number))  # Output: Narcissistic Number
```
**Explanation:** The function `is_narcissistic_number` checks if a number is a narcissistic number by summing the digits raised to the power of the number of digits.

**C++ Code:**
```cpp
#include <iostream>
#include <cmath>
using namespace std;

string isNarcissisticNumber(int number) {
    int originalNumber = number;
    int sum = 0;
    int digits = 0;

    // Count the number of digits
    int temp = number;
    while (temp > 0) {
        digits++;
        temp /= 10;
    }

    // Calculate the narcissistic sum
    temp = number;
    while (temp > 0) {
        int digit = temp % 10;
        sum += pow(digit, digits);
        temp /= 10;
    }

    return (sum == originalNumber) ? "Narcissistic Number" : "Not Narcissistic Number";
}

int main() {
    int number = 153;
    cout << isNarcissisticNumber(number) << endl;  // Output: Narcissistic Number
    return 0;
}
```
**Explanation:** The function `isNarcissisticNumber` follows the same logic as the Python version, using loops to calculate the narcissistic sum.

### 27. Generating a Pattern of Numbers

**Python Code:**
```python
def print_number_pattern(rows):
    for i in range(1, rows + 1):
        print(' '.join(str(j) for j in range(1, i + 1)))

# Example usage
rows = 3
print_number_pattern(rows)
```
**Explanation:** The function `print_number_pattern` generates a number pattern by printing sequential numbers in a loop.

**C++ Code:**
```cpp
#include <iostream>
using namespace std;

void printNumberPattern(int rows) {
    for (int i = 1; i <= rows; ++i) {
        for (int j = 1; j <= i; ++j) {
            cout << j << " ";
        }
        cout << endl;
    }
}

int main() {
    int rows = 3;
    printNumberPattern(rows);
    return 0;
}
```
**Explanation:** The function `printNumberPattern` follows the same logic as the Python version, using nested loops to generate the number pattern.

### 28. Finding the Sum of the Digits of the Factorial of a Number

**Python Code:**
```python
def sum_of_digits_of_factorial(number):
    factorial = 1
    for i in range(1, number + 1):
        factorial *= i
    return sum(int(digit) for digit in str(factorial))

# Example usage
number = 4
print(sum_of_digits_of_factorial(number))  # Output: 6
```
**Explanation:** The function `sum_of_digits_of_factorial` calculates the factorial of a number and then sums its digits.

**C++ Code:**
```cpp
#include <iostream>
#include <string>
using namespace std;

int sumOfDigitsOfFactorial(int number) {
    long long factorial = 1;
    for (int i = 1; i <= number; ++i) {
        factorial *= i;
    }
    int sum = 0;
    string factorialStr = to_string(factorial);
    for (char digit : factorialStr) {
        sum += digit - '0';
    }
    return sum;
}

int main() {
    int number = 4;
    cout << sumOfDigitsOfFactorial(number) << endl;  // Output: 6
    return 0;
}
```
**Explanation:** The function `sumOfDigitsOfFactorial` follows the same logic as the Python version, using loops to calculate the factorial and sum its digits.

### 29. Finding the Largest Palindrome in a String

**Python Code:**
```python
def largest_palindrome(string):
    n = len(string)
    largest = ""
    for i in range(n):
        for j in range(i, n):
            substring = string[i:j+1]
            if substring == substring[::-1] and len(substring) > len(largest):
                largest = substring
    return largest

# Example usage
string = "babad"
print(largest_palindrome(string))  # Output: "bab" or "aba"
```
**Explanation:** The function `largest_palindrome` checks all substrings of a string to find the largest palindrome.

**C++ Code:**
```cpp
#include <iostream>
#include <algorithm>
using namespace std;

string largestPalindrome(const string& str) {
    int n = str.length();
    string largest = "";
    for (int i = 0; i < n; ++i) {
        for (int j = i; j < n; ++j) {
            string substring = str.substr(i, j - i + 1);
            string reversedSubstring = substring;
            reverse(reversedSubstring.begin(), reversedSubstring.end());
            if (substring == reversedSubstring && substring.length() > largest.length()) {
                largest = substring;
            }
        }
    }
    return largest;
}

int main() {
    string str = "babad";
    cout << largestPalindrome(str) << endl;  // Output: "bab" or "aba"
    return 0;
}
```
**Explanation:** The function `largestPalindrome` follows the same logic as the Python version, using nested loops to check all substrings.

### 30. Finding Missing Numbers in a Sequence

**Python Code:**
```python
def find_missing_numbers(sequence):
    n = len(sequence) + 1
    full_sequence = set(range(1, n + 1))
    return list(full_sequence - set(sequence))

# Example usage
sequence = [1, 2, 4, 5]
print(find_missing_numbers(sequence))  # Output: [3]
```
**Explanation:** The function `find_missing_numbers` finds the missing numbers in a sequence by comparing it to a full sequence.

**C++ Code:**
```cpp
#include <iostream>
#include <vector>
#include <set>
using namespace std;

vector<int> findMissingNumbers(const vector<int>& sequence) {
    int n = sequence.size() + 1;
    set<int> fullSequence;
    for (int i = 1; i <= n; ++i) {
        fullSequence.insert(i);
    }
    set<int> sequenceSet(sequence.begin(), sequence.end());
    vector<int> missingNumbers;
    for (int num : fullSequence) {
        if (sequenceSet.find(num) == sequenceSet.end()) {
            missingNumbers.push_back(num);
        }
    }
    return missingNumbers;
}

int main() {
    vector<int> sequence = {1, 2, 4, 5};
    vector<int> missingNumbers = findMissingNumbers(sequence);
    for (int num : missingNumbers) {
        cout << num << " ";
    }
    cout << endl;  // Output: 3
    return 0;
}
```
**Explanation:** The function `findMissingNumbers` follows the same logic as the Python version, using sets to find the missing numbers.

### 31. Generating a Pascal’s Triangle

**Python Code:**
```python
def generate_pascals_triangle(rows):
    triangle = [[1]]
    for i in range(1, rows):
        row = [1]
        for j in range(1, i):
            row.append(triangle[i-1][j-1] + triangle[i-1][j])
        row.append(1)
        triangle.append(row)
    return triangle

# Example usage
rows = 4
for row in generate_pascals_triangle(rows):
    print(row)
```
**Explanation:** The function `generate_pascals_triangle` generates Pascal's Triangle up to a given number of rows.

**C++ Code:**
```cpp
#include <iostream>
#include <vector>
using namespace std;

vector<vector<int>> generatePascalsTriangle(int rows) {
    vector<vector<int>> triangle = {{1}};
    for (int i = 1; i < rows; ++i) {
        vector<int> row = {1};
        for (int j = 1; j < i; ++j) {
            row.push_back(triangle[i-1][j-1] + triangle[i-1][j]);
        }
        row.push_back(1);
        triangle.push_back(row);
    }
    return triangle;
}

int main() {
    int rows = 4;
    vector<vector<int>> triangle = generatePascalsTriangle(rows);
    for (const auto& row : triangle) {
        for (int num : row) {
            cout << num << " ";
        }
        cout << endl;
    }
    return 0;
}
```
**Explanation:** The function `generatePascalsTriangle` follows the same logic as the Python version, using nested loops to generate the triangle.

### 32. Finding the Median of an Array

**Python Code:**
```python
def find_median(array):
    sorted_array = sorted(array)
    n = len(sorted_array)
    if n % 2 == 1:
        return sorted_array[n // 2]
    else:
        return (sorted_array[n // 2 - 1] + sorted_array[n // 2]) / 2

# Example usage
array = [3, 1, 2, 4, 5]
print(find_median(array))  # Output: 3
```
**Explanation:** The function `find_median` sorts the array and finds the median value.

**C++ Code:**
```cpp
#include <iostream>
#include <vector>
#include <algorithm>
using namespace std;

double findMedian(vector<int> array) {
    sort(array.begin(), array.end());
    int n = array.size();
    if (n % 2 == 1) {
        return array[n / 2];
    } else {
        return (array[n / 2 - 1] + array[n / 2]) / 2.0;
    }
}

int main() {
    vector<int> array = {3, 1, 2, 4, 5};
    cout << findMedian(array) << endl;  // Output: 3
    return 0;
}
```
**Explanation:** The function `findMedian` follows the same logic as the Python version, using sorting to find the median.

### 33. Calculating the Power of a Number

**Python Code:**
```python
def power(base, exponent):
    return base ** exponent

# Example usage
base = 2
exponent = 3
print(power(base, exponent))  # Output: 8
```
**Explanation:** The function `power` calculates the power of a number using the `**` operator.

**C++ Code:**
```cpp
#include <iostream>
#include <cmath>
using namespace std;

double power(double base, int exponent) {
    return pow(base, exponent);
}

int main() {
    double base = 2;
    int exponent = 3;
    cout << power(base, exponent) << endl;  // Output: 8
    return 0;
}
```
**Explanation:** The function `power` uses the `pow` function from the cmath library to calculate the power of a number.

### 34. Checking for an Anagram

**Python Code:**
```python
def is_anagram(string1, string2):
    return sorted(string1) == sorted(string2)

# Example usage
string1 = "listen"
string2 = "silent"
print(is_anagram(string1, string2))  # Output: True
```
**Explanation:** The function `is_anagram` checks if two strings are anagrams by sorting and comparing them.

**C++ Code:**
```cpp
#include <iostream>
#include <algorithm>
using namespace std;

bool isAnagram(string str1, string str2) {
    sort(str1.begin(), str1.end());
    sort(str2.begin(), str2.end());
    return str1 == str2;
}

int main() {
    string str1 = "listen";
    string str2 = "silent";
    cout << isAnagram(str1, str2) << endl;  // Output: 1 (True)
    return 0;
}
```
**Explanation:** The function `isAnagram` follows the same logic as the Python version, using sorting to check for anagrams.

### 35. Finding the Sum of Prime Numbers in a Range

**Python Code:**
```python
def sum_of_primes(range_start, range_end):
    def is_prime(num):
        if num <= 1:
            return False
        for i in range(2, int(num ** 0.5) + 1):
            if num % i == 0:
                return False
        return True

    return sum(num for num in range(range_start, range_end + 1) if is_prime(num))

# Example usage
range_start = 1
range_end = 10
print(sum_of_primes(range_start, range_end))  # Output: 17
```
**Explanation:** The function `sum_of_primes` uses a helper function `is_prime` to check for prime numbers and sums them within a range.

**C++ Code:**
```cpp
#include <iostream>
#include <cmath>
using namespace std;

bool isPrime(int num) {
    if (num <= 1) {
        return false;
    }
    for (int i = 2; i <= sqrt(num); ++i) {
        if (num % i == 0) {
            return false;
        }
    }
    return true;
}

int sumOfPrimes(int rangeStart, int rangeEnd) {
    int sum = 0;
    for (int num = rangeStart; num <= rangeEnd; ++num) {
        if (isPrime(num)) {
            sum += num;
        }
    }
    return sum;
}

int main() {
    int rangeStart = 1;
    int rangeEnd = 10;
    cout << sumOfPrimes(rangeStart, rangeEnd) << endl;  // Output: 17
    return 0;
}
```
**Explanation:** The function `sumOfPrimes` follows the same logic as the Python version, using a helper function `isPrime` to check for prime numbers.

### 36. Finding the N-th Triangular Number

**Python Code:**
```python
def triangular_number(n):
    return n * (n + 1) // 2

# Example usage
n = 4
print(triangular_number(n))  # Output: 10
```
**Explanation:** The function `triangular_number` calculates the N-th triangular number using the formula.

**C++ Code:**
```cpp
#include <iostream>
using namespace std;

int triangularNumber(int n) {
    return n * (n + 1) / 2;
}

int main() {
    int n = 4;
    cout << triangularNumber(n) << endl;  // Output: 10
    return 0;
}
```
**Explanation:** The function `triangularNumber` follows the same logic as the Python version, using the formula to calculate the N-th triangular number.

### 37. Checking for Perfect Squares

**Python Code:**
```python
def is_perfect_square(number):
    root = int(number ** 0.5)
    return root * root == number

# Example usage
number = 16
print(is_perfect_square(number))  # Output: True
```
**Explanation:** The function `is_perfect_square` checks if a number is a perfect square by comparing the square of the integer square root to the number.

**C++ Code:**
```cpp
#include <iostream>
#include <cmath>
using namespace std;

bool isPerfectSquare(int number) {
    int root = sqrt(number);
    return root * root == number;
}

int main() {
    int number = 16;
    cout << isPerfectSquare(number) << endl;  // Output: 1 (True)
    return 0;
}
```
**Explanation:** The function `isPerfectSquare` follows the same logic as the Python version, using the square root to check for perfect squares.

### 38. Finding the Sum of Squares of Digits

**Python Code:**
```python
def sum_of_squares_of_digits(number):
    return sum(int(digit) ** 2 for digit in str(number))

# Example usage
number = 123
print(sum_of_squares_of_digits(number))  # Output: 14
```
**Explanation:** The function `sum_of_squares_of_digits` calculates the sum of the squares of the digits of a number.

**C++ Code:**
```cpp
#include <iostream>
using namespace std;

int sumOfSquaresOfDigits(int number) {
    int sum = 0;
    while (number > 0) {
        int digit = number % 10;
        sum += digit * digit;
        number /= 10;
    }
    return sum;
}

int main() {
    int number = 123;
    cout << sumOfSquaresOfDigits(number) << endl;  // Output: 14
    return 0;
}
```
**Explanation:** The function `sumOfSquaresOfDigits` follows the same logic as the Python version, using a loop to calculate the sum of the squares of the digits.

### 39. Generating a Square Matrix of a Given Size

**Python Code:**
```python
def generate_square_matrix(size):
    matrix = [[(i * size + j + 1) for j in range(size)] for i in range(size)]
    return matrix

# Example usage
size = 3
for row in generate_square_matrix(size):
    print(row)
```
**Explanation:** The function `generate_square_matrix` generates a square matrix of a given size filled with sequential numbers.

**C++ Code:**
```cpp
#include <iostream>
#include <vector>
using namespace std;

vector<vector<int>> generateSquareMatrix(int size) {
    vector<vector<int>> matrix(size, vector<int>(size));
    for (int i = 0; i < size; ++i) {
        for (int j = 0; j < size; ++j) {
            matrix[i][j] = i * size + j + 1;
        }
    }
    return matrix;
}

int main() {
    int size = 3;
    vector<vector<int>> matrix = generateSquareMatrix(size);
    for (const auto& row : matrix) {
        for (int num : row) {
            cout << num << " ";
        }
        cout << endl;
    }
    return 0;
}
```
**Explanation:** The function `generateSquareMatrix` follows the same logic as the Python version, using nested loops to generate the matrix.

### 40. Calculating the Sum of Digits of a Number Until Single Digit

**Python Code:**
```python
def sum_of_digits_until_single(number):
    while number >= 10:
        number = sum(int(digit) for digit in str(number))
    return number

# Example usage
number = 9875
print(sum_of_digits_until_single(number))  # Output: 2
```
**Explanation:** The function `sum_of_digits_until_single` repeatedly sums the digits of a number until a single digit is obtained.

**C++ Code:**
```cpp
#include <iostream>
using namespace std;

int sumOfDigitsUntilSingle(int number) {
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
    int number = 9875;
    cout << sumOfDigitsUntilSingle(number) << endl;  // Output: 2
    return 0;
}
```
**Explanation:** The function `sumOfDigitsUntilSingle` follows the same logic as the Python version, using loops to sum the digits until a single digit is obtained.

### 41. Finding the Count of Specific Digits in a Number

**Python Code:**
```python
def count_specific_digit(number, digit):
    return str(number).count(str(digit))

# Example usage
number = 122333
digit = 3
print(count_specific_digit(number, digit))  # Output: 3
```
**Explanation:** The function `count_specific_digit` converts the number to a string and counts the occurrences of a specific digit.

**C++ Code:**
```cpp
#include <iostream>
#include <string>
using namespace std;

int countSpecificDigit(int number, int digit) {
    int count = 0;
    string numberStr = to_string(number);
    for (char ch : numberStr) {
        if (ch - '0' == digit) {
            count++;
        }
    }
    return count;
}

int main() {
    int number = 122333;
    int digit = 3;
    cout << countSpecificDigit(number, digit) << endl;  // Output: 3
    return 0;
}
```
**Explanation:** The function `countSpecificDigit` follows the same logic as the Python version, using a loop to count the occurrences of a specific digit.

### 42. Generating a Fibonacci Sequence Using Recursion

**Python Code:**
```python
def fibonacci_recursive(n):
    if n <= 0:
        return []
    elif n == 1:
        return [0]
    elif n == 2:
        return [0, 1]
    else:
        seq = fibonacci_recursive(n - 1)
        seq.append(seq[-1] + seq[-2])
        return seq

# Example usage
n = 5
print(fibonacci_recursive(n))  # Output: [0, 1, 1, 2, 3]
```
**Explanation:** The function `fibonacci_recursive` generates the Fibonacci sequence up to a given number using recursion.

**C++ Code:**
```cpp
#include <iostream>
#include <vector>
using namespace std;

vector<int> fibonacciRecursive(int n) {
    if (n <= 0) {
        return {};
    } else if (n == 1) {
        return {0};
    } else if (n == 2) {
        return {0, 1};
    } else {
        vector<int> seq = fibonacciRecursive(n - 1);
        seq.push_back(seq.back() + *(seq.end() - 2));
        return seq;
    }
}

int main() {
    int n = 5;
    vector<int> seq = fibonacciRecursive(n);
    for (int num : seq) {
        cout << num << " ";
    }
    cout << endl;  // Output: 0 1 1 2 3
    return 0;
}
```
**Explanation:** The function `fibonacciRecursive` follows the same logic as the Python version, using recursion to generate the Fibonacci sequence.

### 43. Finding All Divisors of a Number

**Python Code:**
```python
def find_divisors(number):
    return [i for i in range(1, number + 1) if number % i == 0]

# Example usage
number = 12
print(find_divisors(number))  # Output: [1, 2, 3, 4, 6, 12]
```
**Explanation:** The function `find_divisors` finds all divisors of a number using a list comprehension.

**C++ Code:**
```cpp
#include <iostream>
#include <vector>
using namespace std;

vector<int> findDivisors(int number) {
    vector<int> divisors;
    for (int i = 1; i <= number; ++i) {
        if (number % i == 0) {
            divisors.push_back(i);
        }
    }
    return divisors;
}

int main() {
    int number = 12;
    vector<int> divisors = findDivisors(number);
    for (int divisor : divisors) {
        cout << divisor << " ";
    }
    cout << endl;  // Output: 1 2 3 4 6 12
    return 0;
}
```
**Explanation:** The function `findDivisors` follows the same logic as the Python version, using a loop to find all divisors.

### 44. Finding the Average of Numbers in an Array

**Python Code:**
```python
def find_average(array):
    return sum(array) / len(array)

# Example usage
array = [1, 2, 3, 4, 5]
print(find_average(array))  # Output: 3.0
```
**Explanation:** The function `find_average` calculates the average of numbers in an array.

**C++ Code:**
```cpp
#include <iostream>
#include <vector>
#include <numeric>
using namespace std;

double findAverage(const vector<int>& array) {
    return accumulate(array.begin(), array.end(), 0.0) / array.size();
}

int main() {
    vector<int> array = {1, 2, 3, 4, 5};
    cout << findAverage(array) << endl;  // Output: 3.0
    return 0;
}
```
**Explanation:** The function `findAverage` follows the same logic as the Python version, using the `accumulate` function to calculate the average.

### 45. Finding the Mode of Numbers in an Array

**Python Code:**
```python
from collections import Counter

def find_mode(array):
    count = Counter(array)
    max_count = max(count.values())
    mode = [num for num, freq in count.items() if freq == max_count]
    return mode

# Example usage
array = [1, 2, 2, 3, 4, 4, 4]
print(find_mode(array))  # Output: [4]
```
**Explanation:** The function `find_mode` uses the `Counter` class to find the mode of numbers in an array.

**C++ Code:**
```cpp
#include <iostream>
#include <vector>
#include <unordered_map>
#include <algorithm>
using namespace std;

vector<int> findMode(const vector<int>& array) {
    unordered_map<int, int> count;
    for (int num : array) {
        count[num]++;
    }
    int max_count = 0;
    for (const auto& pair : count) {
        max_count = max(max_count, pair.second);
    }
    vector<int> mode;
    for (const auto& pair : count) {
        if (pair.second == max_count) {
            mode.push_back(pair.first);
        }
    }
    return mode;
}

int main() {
    vector<int> array = {1, 2, 2, 3, 4, 4, 4};
    vector<int> mode = findMode(array);
    for (int num : mode) {
        cout << num << " ";
    }
    cout << endl;  // Output: 4
    return 0;
}
```
**Explanation:** The function `findMode` follows the same logic as the Python version, using an unordered map to count frequencies and find the mode.

### 46. Determining the Length of a String Without Using Built-In Functions

**Python Code:**
```python
def string_length(string):
    count = 0
    for _ in string:
        count += 1
    return count

# Example usage
string = "hello"
print(string_length(string))  # Output: 5
```
**Explanation:** The function `string_length` iterates through the string to determine its length without using built-in functions.

**C++ Code:**
```cpp
#include <iostream>
using namespace std;

int stringLength(const string& str) {
    int count = 0;
    for (char ch : str) {
        count++;
    }
    return count;
}

int main() {
    string str = "hello";
    cout << stringLength(str) << endl;  // Output: 5
    return 0;
}
```
**Explanation:** The function `stringLength` follows the same logic as the Python version, using a loop to determine the length of the string.

### 47. Generating a Number Pyramid

**Python Code:**
```python
def print_number_pyramid(rows):
    for i in range(1, rows + 1):
        print(' '.join(str(j) for j in range(1, i + 1)))

# Example usage
rows = 4
print_number_pyramid(rows)
```
**Explanation:** The function `print_number_pyramid` generates a number pyramid by printing sequential numbers in a loop.

**C++ Code:**
```cpp
#include <iostream>
using namespace std;

void printNumberPyramid(int rows) {
    for (int i = 1; i <= rows; ++i) {
        for (int j = 1; j <= i; ++j) {
            cout << j << " ";
        }
        cout << endl;
    }
}

int main() {
    int rows = 4;
    printNumberPyramid(rows);
    return 0;
}
```
**Explanation:** The function `printNumberPyramid` follows the same logic as the Python version, using nested loops to generate the number pyramid.

### 48. Finding the Sum of Prime Factors of a Number

**Python Code:**
```python
def sum_of_prime_factors(number):
    def is_prime(num):
        if num <= 1:
            return False
        for i in range(2, int(num ** 0.5) + 1):
            if num % i == 0:
                return False
        return True

    prime_factors = [i for i in range(2, number + 1) if number % i == 0 and is_prime(i)]
    return sum(prime_factors)

# Example usage
number = 12
print(sum_of_prime_factors(number))  # Output: 5
```
**Explanation:** The function `sum_of_prime_factors` finds all prime factors of a number and sums them.

**C++ Code:**
```cpp
#include <iostream>
#include <cmath>
#include <vector>
using namespace std;

bool isPrime(int num) {
    if (num <= 1) {
        return false;
    }
    for (int i = 2; i <= sqrt(num); ++i) {
        if (num % i == 0) {
            return false;
        }
    }
    return true;
}

int sumOfPrimeFactors(int number) {
    vector<int> primeFactors;
    for (int i = 2; i <= number; ++i) {
        if (number % i == 0 && isPrime(i)) {
            primeFactors.push_back(i);
        }
    }
    int sum = 0;
    for (int factor : primeFactors) {
        sum += factor;
    }
    return sum;
}

int main() {
    int number = 12;
    cout << sumOfPrimeFactors(number) << endl;  // Output: 5
    return 0;
}
```
**Explanation:** The function `sumOfPrimeFactors` follows the same logic as the Python version, using a loop to find and sum the prime factors.

### 49. Finding the Second Largest Number in an Array

**Python Code:**
```python
def second_largest(array):
    unique_numbers = list(set(array))
    unique_numbers.sort(reverse=True)
    return unique_numbers[1] if len(unique_numbers) > 1 else None

# Example usage
array = [10, 20, 4, 45, 99]
print(second_largest(array))  # Output: 45
```
**Explanation:** The function `second_largest` finds the second largest number in an array by sorting the unique numbers in descending order.

**C++ Code:**
```cpp
#include <iostream>
#include <vector>
#include <algorithm>
#include <set>
using namespace std;

int secondLargest(const vector<int>& array) {
    set<int> uniqueNumbers(array.begin(), array.end());
    if (uniqueNumbers.size() < 2) {
        return -1;  // Return -1 if there is no second largest number
    }
    auto it = uniqueNumbers.rbegin();
    advance(it, 1);
    return *it;
}

int main() {
    vector<int> array = {10, 20, 4, 45, 99};
    cout << secondLargest(array) << endl;  // Output: 45
    return 0;
}
```
**Explanation:** The function `secondLargest` follows the same logic as the Python version, using a set to find the second largest number.

### 50. Finding the Longest Substring Without Repeating Characters

**Python Code:**
```python
def longest_substring_without_repeating_characters(string):
    char_index_map = {}
    start = 0
    max_length = 0
    max_substring = ""

    for end in range(len(string)):
        if string[end] in char_index_map:
            start = max(start, char_index_map[string[end]] + 1)
        char_index_map[string[end]] = end
        if end - start + 1 > max_length:
            max_length = end - start + 1
            max_substring = string[start:end+1]

    return max_substring

# Example usage
string = "abcabcbb"
print(longest_substring_without_repeating_characters(string))  # Output: "abc"
```
**Explanation:** The function `longest_substring_without_repeating_characters` uses a sliding window approach to find the longest substring without repeating characters.

**C++ Code:**
```cpp
#include <iostream>
#include <unordered_map>
#include <string>
using namespace std;

string longestSubstringWithoutRepeatingCharacters(const string& str) {
    unordered_map<char, int> charIndexMap;
    int start = 0;
    int maxLength = 0;
    string maxSubstring = "";

    for (int end = 0; end < str.length(); ++end) {
        if (charIndexMap.find(str[end]) != charIndexMap.end()) {
            start = max(start, charIndexMap[str[end]] + 1);
        }
        charIndexMap[str[end]] = end;
        if (end - start + 1 > maxLength) {
            maxLength = end - start + 1;
            maxSubstring = str.substr(start, maxLength);
        }
    }
    return maxSubstring;
}

int main() {
    string str = "abcabcbb";
    cout << longestSubstringWithoutRepeatingCharacters(str) << endl;  // Output: "abc"
    return 0;
}
```
**Explanation:** The function `longestSubstringWithoutRepeatingCharacters` follows the same logic as the Python version, using a sliding window approach to find the longest substring without repeating characters.