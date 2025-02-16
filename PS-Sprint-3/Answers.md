Let's go through each problem, providing both Python and C++ code with explanations for each line.

### Problem 1: Print a Right-Angle Triangle of Stars

**Python Code:**

```python
def print_right_angle_triangle(n):
    for i in range(1, n + 1):  # Loop from 1 to n (inclusive)
        print('*' * i)  # Print '*' multiplied by the current row number

# Example usage
print_right_angle_triangle(4)
```

**Explanation:**
- `def print_right_angle_triangle(n):` defines a function that takes an integer `n`.
- `for i in range(1, n + 1):` iterates from 1 to `n`.
- `print('*' * i)` prints a string of `*` characters, repeated `i` times for each row.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printRightAngleTriangle(int n) {
    for (int i = 1; i <= n; i++) {  // Loop from 1 to n (inclusive)
        for (int j = 1; j <= i; j++) {  // Loop to print '*' i times
            cout << "*";
        }
        cout << endl;  // Move to the next line after printing stars
    }
}

int main() {
    printRightAngleTriangle(4);  // Example usage
    return 0;
}
```

**Explanation:**
- `#include <iostream>` includes the input-output stream library.
- `using namespace std;` allows using standard library functions without the `std::` prefix.
- `void printRightAngleTriangle(int n)` defines a function that takes an integer `n`.
- `for (int i = 1; i <= n; i++)` iterates from 1 to `n`.
- `for (int j = 1; j <= i; j++)` prints `*` characters `i` times for each row.
- `cout << endl;` moves to the next line after printing stars.

### Problem 2: Print a Square of Stars

**Python Code:**

```python
def print_square(n):
    for _ in range(n):  # Loop n times for rows
        print('*' * n)  # Print '*' multiplied by n for each row

# Example usage
print_square(5)
```

**Explanation:**
- `def print_square(n):` defines a function that takes an integer `n`.
- `for _ in range(n):` iterates `n` times for the number of rows.
- `print('*' * n)` prints a string of `*` characters, repeated `n` times for each row.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printSquare(int n) {
    for (int i = 0; i < n; i++) {  // Loop n times for rows
        for (int j = 0; j < n; j++) {  // Loop n times for columns
            cout << "*";
        }
        cout << endl;  // Move to the next line after printing stars
    }
}

int main() {
    printSquare(5);  // Example usage
    return 0;
}
```

**Explanation:**
- `#include <iostream>` includes the input-output stream library.
- `using namespace std;` allows using standard library functions without the `std::` prefix.
- `void printSquare(int n)` defines a function that takes an integer `n`.
- `for (int i = 0; i < n; i++)` iterates `n` times for the number of rows.
- `for (int j = 0; j < n; j++)` prints `*` characters `n` times for each column.
- `cout << endl;` moves to the next line after printing stars.

### Problem 3: Print a Pyramid Pattern

**Python Code:**

```python
def print_pyramid(n):
    for i in range(n):  # Loop from 0 to n-1
        spaces = ' ' * (n - i - 1)  # Calculate leading spaces
        stars = '*' * (2 * i + 1)  # Calculate stars
        print(spaces + stars)  # Print spaces followed by stars

# Example usage
print_pyramid(3)
```

**Explanation:**
- `def print_pyramid(n):` defines a function that takes an integer `n`.
- `for i in range(n):` iterates from 0 to `n-1`.
- `spaces = ' ' * (n - i - 1)` calculates the number of leading spaces.
- `stars = '*' * (2 * i + 1)` calculates the number of stars.
- `print(spaces + stars)` prints the spaces followed by stars.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printPyramid(int n) {
    for (int i = 0; i < n; i++) {  // Loop from 0 to n-1
        for (int j = 0; j < n - i - 1; j++) {  // Print leading spaces
            cout << " ";
        }
        for (int k = 0; k < 2 * i + 1; k++) {  // Print stars
            cout << "*";
        }
        cout << endl;  // Move to the next line after printing stars
    }
}

int main() {
    printPyramid(3);  // Example usage
    return 0;
}
```

**Explanation:**
- `#include <iostream>` includes the input-output stream library.
- `using namespace std;` allows using standard library functions without the `std::` prefix.
- `void printPyramid(int n)` defines a function that takes an integer `n`.
- `for (int i = 0; i < n; i++)` iterates from 0 to `n-1`.
- `for (int j = 0; j < n - i - 1; j++)` prints leading spaces.
- `for (int k = 0; k < 2 * i + 1; k++)` prints stars.
- `cout << endl;` moves to the next line after printing stars.

### Problem 4: Print a Diamond Pattern

**Python Code:**

```python
def print_diamond(n):
    for i in range(n):  # Loop for the upper part of the diamond
        spaces = ' ' * (n - i - 1)  # Calculate leading spaces
        stars = '*' * (2 * i + 1)  # Calculate stars
        print(spaces + stars)  # Print spaces followed by stars
    for i in range(n - 2, -1, -1):  # Loop for the lower part of the diamond
        spaces = ' ' * (n - i - 1)  # Calculate leading spaces
        stars = '*' * (2 * i + 1)  # Calculate stars
        print(spaces + stars)  # Print spaces followed by stars

# Example usage
print_diamond(3)
```

**Explanation:**
- `def print_diamond(n):` defines a function that takes an integer `n`.
- `for i in range(n):` iterates from 0 to `n-1` for the upper part of the diamond.
- `spaces = ' ' * (n - i - 1)` calculates the number of leading spaces.
- `stars = '*' * (2 * i + 1)` calculates the number of stars.
- `print(spaces + stars)` prints the spaces followed by stars.
- `for i in range(n - 2, -1, -1):` iterates from `n-2` to 0 for the lower part of the diamond.
- The same logic is applied for the lower part as for the upper part.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printDiamond(int n) {
    for (int i = 0; i < n; i++) {  // Loop for the upper part of the diamond
        for (int j = 0; j < n - i - 1; j++) {  // Print leading spaces
            cout << " ";
        }
        for (int k = 0; k < 2 * i + 1; k++) {  // Print stars
            cout << "*";
        }
        cout << endl;  // Move to the next line after printing stars
    }
    for (int i = n - 2; i >= 0; i--) {  // Loop for the lower part of the diamond
        for (int j = 0; j < n - i - 1; j++) {  // Print leading spaces
            cout << " ";
        }
        for (int k = 0; k < 2 * i + 1; k++) {  // Print stars
            cout << "*";
        }
        cout << endl;  // Move to the next line after printing stars
    }
}

int main() {
    printDiamond(3);  // Example usage
    return 0;
}
```

**Explanation:**
- `#include <iostream>` includes the input-output stream library.
- `using namespace std;` allows using standard library functions without the `std::` prefix.
- `void printDiamond(int n)` defines a function that takes an integer `n`.
- `for (int i = 0; i < n; i++)` iterates from 0 to `n-1` for the upper part of the diamond.
- `for (int j = 0; j < n - i - 1; j++)` prints leading spaces.
- `for (int k = 0; k < 2 * i + 1; k++)` prints stars.
- `cout << endl;` moves to the next line after printing stars.
- `for (int i = n - 2; i >= 0; i--)` iterates from `n-2` to 0 for the lower part of the diamond.
- The same logic is applied for the lower part as for the upper part.

### Problem 5: Print a Hollow Square of Stars

**Python Code:**

```python
def print_hollow_square(n):
    for i in range(n):  # Loop from 0 to n-1
        if i == 0 or i == n - 1:  # Print full row of stars for the first and last rows
            print('*' * n)
        else:  # Print stars at the borders and spaces in between
            print('*' + ' ' * (n - 2) + '*')

# Example usage
print_hollow_square(5)
```

**Explanation:**
- `def print_hollow_square(n):` defines a function that takes an integer `n`.
- `for i in range(n):` iterates from 0 to `n-1`.
- `if i == 0 or i == n - 1:` checks if the current row is the first or last row.
- `print('*' * n)` prints a full row of stars for the first and last rows.
- `else:` handles the rows in between.
- `print('*' + ' ' * (n - 2) + '*')` prints stars at the borders and spaces in between.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printHollowSquare(int n) {
    for (int i = 0; i < n; i++) {  // Loop from 0 to n-1
        if (i == 0 || i == n - 1) {  // Print full row of stars for the first and last rows
            for (int j = 0; j < n; j++) {
                cout << "*";
            }
        } else {  // Print stars at the borders and spaces in between
            cout << "*";
            for (int j = 0; j < n - 2; j++) {
                cout << " ";
            }
            cout << "*";
        }
        cout << endl;  // Move to the next line after printing stars
    }
}

int main() {
    printHollowSquare(5);  // Example usage
    return 0;
}
```

**Explanation:**
- `#include <iostream>` includes the input-output stream library.
- `using namespace std;` allows using standard library functions without the `std::` prefix.
- `void printHollowSquare(int n)` defines a function that takes an integer `n`.
- `for (int i = 0; i < n; i++)` iterates from 0 to `n-1`.
- `if (i == 0 || i == n - 1):` checks if the current row is the first or last row.
- `for (int j = 0; j < n; j++)` prints a full row of stars for the first and last rows.
- `else:` handles the rows in between.
- `cout << "*";` prints a star at the border.
- `for (int j = 0; j < n - 2; j++)` prints spaces in between.
- `cout << "*";` prints a star at the border.
- `cout << endl;` moves to the next line after printing stars.

### Problem 6: Print a Number Triangle

**Python Code:**

```python
def print_number_triangle(n):
    num = 1  # Initialize the starting number
    for i in range(1, n + 1):  # Loop from 1 to n (inclusive)
        print(''.join(str(min(num + j, 9)) for j in range(i)))  # Print numbers in the current row
        num += i  # Increment the starting number for the next row

# Example usage
print_number_triangle(4)
```

**Explanation:**
- `def print_number_triangle(n):` defines a function that takes an integer `n`.
- `num = 1` initializes the starting number.
- `for i in range(1, n + 1):` iterates from 1 to `n`.
- `print(''.join(str(min(num + j, 9)) for j in range(i)))` prints numbers in the current row.
- `num += i` increments the starting number for the next row.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printNumberTriangle(int n) {
    int num = 1;  // Initialize the starting number
    for (int i = 1; i <= n; i++) {  // Loop from 1 to n (inclusive)
        for (int j = 0; j < i; j++) {  // Loop to print numbers in the current row
            cout << min(num + j, 9);
        }
        num += i;  // Increment the starting number for the next row
        cout << endl;  // Move to the next line after printing numbers
    }
}

int main() {
    printNumberTriangle(4);  // Example usage
    return 0;
}
```

**Explanation:**
- `#include <iostream>` includes the input-output stream library.
- `using namespace std;` allows using standard library functions without the `std::` prefix.
- `void printNumberTriangle(int n)` defines a function that takes an integer `n`.
- `int num = 1;` initializes the starting number.
- `for (int i = 1; i <= n; i++)` iterates from 1 to `n`.
- `for (int j = 0; j < i; j++)` prints numbers in the current row.
- `cout << min(num + j, 9);` prints the minimum of `num + j` and 9.
- `num += i;` increments the starting number for the next row.
- `cout << endl;` moves to the next line after printing numbers.

### Problem 7: Print an Inverted Triangle Pattern

**Python Code:**

```python
def print_inverted_triangle(n):
    for i in range(n, 0, -1):  # Loop from n to 1 (inclusive)
        spaces = ' ' * (n - i)  # Calculate leading spaces
        stars = '*' * (2 * i - 1)  # Calculate stars
        print(spaces + stars)  # Print spaces followed by stars

# Example usage
print_inverted_triangle(5)
```

**Explanation:**
- `def print_inverted_triangle(n):` defines a function that takes an integer `n`.
- `for i in range(n, 0, -1):` iterates from `n` to 1.
- `spaces = ' ' * (n - i)` calculates the number of leading spaces.
- `stars = '*' * (2 * i - 1)` calculates the number of stars.
- `print(spaces + stars)` prints the spaces followed by stars.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printInvertedTriangle(int n) {
    for (int i = n; i >= 1; i--) {  // Loop from n to 1 (inclusive)
        for (int j = 0; j < n - i; j++) {  // Print leading spaces
            cout << " ";
        }
        for (int k = 0; k < 2 * i - 1; k++) {  // Print stars
            cout << "*";
        }
        cout << endl;  // Move to the next line after printing stars
    }
}

int main() {
    printInvertedTriangle(5);  // Example usage
    return 0;
}
```

**Explanation:**
- `#include <iostream>` includes the input-output stream library.
- `using namespace std;` allows using standard library functions without the `std::` prefix.
- `void printInvertedTriangle(int n)` defines a function that takes an integer `n`.
- `for (int i = n; i >= 1; i--)` iterates from `n` to 1.
- `for (int j = 0; j < n - i; j++)` prints leading spaces.
- `for (int k = 0; k < 2 * i - 1; k++)` prints stars.
- `cout << endl;` moves to the next line after printing stars.

### Problem 8: Print a Diamond Pattern with Numbers

**Python Code:**

```python
def print_diamond_with_numbers(n):
    for i in range(n):  # Loop for the upper part of the diamond
        spaces = ' ' * (n - i - 1)  # Calculate leading spaces
        numbers = ''.join(str(i + j + 1) for j in range(i + 1))  # Calculate numbers
        print(spaces + numbers + numbers[-2::-1])  # Print spaces followed by numbers and their reverse
    for i in range(n - 2, -1, -1):  # Loop for the lower part of the diamond
        spaces = ' ' * (n - i - 1)  # Calculate leading spaces
        numbers = ''.join(str(i + j + 1) for j in range(i + 1))  # Calculate numbers
        print(spaces + numbers + numbers[-2::-1])  # Print spaces followed by numbers and their reverse

# Example usage
print_diamond_with_numbers(3)
```

**Explanation:**
- `def print_diamond_with_numbers(n):` defines a function that takes an integer `n`.
- `for i in range(n):` iterates from 0 to `n-1` for the upper part of the diamond.
- `spaces = ' ' * (n - i - 1)` calculates the number of leading spaces.
- `numbers = ''.join(str(i + j + 1) for j in range(i + 1))` calculates the numbers.
- `print(spaces + numbers + numbers[-2::-1])` prints the spaces followed by numbers and their reverse.
- `for i in range(n - 2, -1, -1):` iterates from `n-2` to 0 for the lower part of the diamond.
- The same logic is applied for the lower part as for the upper part.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printDiamondWithNumbers(int n) {
    for (int i = 0; i < n; i++) {  // Loop for the upper part of the diamond
        for (int j = 0; j < n - i - 1; j++) {  // Print leading spaces
            cout << " ";
        }
        for (int k = 0; k <= i; k++) {  // Print numbers
            cout << i + k + 1;
        }
        for (int k = i - 1; k >= 0; k--) {  // Print reverse of numbers
            cout << i + k + 1;
        }
        cout << endl;  // Move to the next line after printing numbers
    }
    for (int i = n - 2; i >= 0; i--) {  // Loop for the lower part of the diamond
        for (int j = 0; j < n - i - 1; j++) {  // Print leading spaces
            cout << " ";
        }
        for (int k = 0; k <= i; k++) {  // Print numbers
            cout << i + k + 1;
        }
        for (int k = i - 1; k >= 0; k--) {  // Print reverse of numbers
            cout << i + k + 1;
        }
        cout << endl;  // Move to the next line after printing numbers
    }
}

int main() {
    printDiamondWithNumbers(3);  // Example usage
    return 0;
}
```

**Explanation:**
- `#include <iostream>` includes the input-output stream library.
- `using namespace std;` allows using standard library functions without the `std::` prefix.
- `void printDiamondWithNumbers(int n)` defines a function that takes an integer `n`.
- `for (int i = 0; i < n; i++)` iterates from 0 to `n-1` for the upper part of the diamond.
- `for (int j = 0; j < n - i - 1; j++)` prints leading spaces.
- `for (int k = 0; k <= i; k++)` prints numbers.
- `for (int k = i - 1; k >= 0; k--)` prints the reverse of numbers.
- `cout << endl;` moves to the next line after printing numbers.
- `for (int i = n - 2; i >= 0; i--)` iterates from `n-2` to 0 for the lower part of the diamond.
- The same logic is applied for the lower part as for the upper part.

### Problem 9: Print a Right-Angle Triangle of Numbers

**Python Code:**

```python
def print_right_angle_triangle_of_numbers(n):
    num = 1  # Initialize the starting number
    for i in range(1, n + 1):  # Loop from 1 to n (inclusive)
        row = ''.join(str(num + j) for j in range(i))  # Calculate numbers in the current row
        print(row)  # Print the current row
        num += i  # Increment the starting number for the next row

# Example usage
print_right_angle_triangle_of_numbers(4)
```

**Explanation:**
- `def print_right_angle_triangle_of_numbers(n):` defines a function that takes an integer `n`.
- `num = 1` initializes the starting number.
- `for i in range(1, n + 1):` iterates from 1 to `n`.
- `row = ''.join(str(num + j) for j in range(i))` calculates the numbers in the current row.
- `print(row)` prints the current row.
- `num += i` increments the starting number for the next row.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printRightAngleTriangleOfNumbers(int n) {
    int num = 1;  // Initialize the starting number
    for (int i = 1; i <= n; i++) {  // Loop from 1 to n (inclusive)
        for (int j = 0; j < i; j++) {  // Loop to print numbers in the current row
            cout << num + j;
        }
        num += i;  // Increment the starting number for the next row
        cout << endl;  // Move to the next line after printing numbers
    }
}

int main() {
    printRightAngleTriangleOfNumbers(4);  // Example usage
    return 0;
}
```

**Explanation:**
- `#include <iostream>` includes the input-output stream library.
- `using namespace std;` allows using standard library functions without the `std::` prefix.
- `void printRightAngleTriangleOfNumbers(int n)` defines a function that takes an integer `n`.
- `int num = 1;` initializes the starting number.
- `for (int i = 1; i <= n; i++)` iterates from 1 to `n`.
- `for (int j = 0; j < i; j++)` prints numbers in the current row.
- `cout << num + j;` prints the current number.
- `num += i;` increments the starting number for the next row.
- `cout << endl;` moves to the next line after printing numbers.

### Problem 10: Print a Pyramid Pattern with Numbers

**Python Code:**

```python
def print_pyramid_with_numbers(n):
    num = 1  # Initialize the starting number
    for i in range(n):  # Loop from 0 to n-1
        spaces = ' ' * (n - i - 1)  # Calculate leading spaces
        numbers = ''.join(str(num + j) for j in range(2 * i + 1))  # Calculate numbers
        print(spaces + numbers)  # Print spaces followed by numbers
        num += 2 * i + 1  # Increment the starting number for the next row

# Example usage
print_pyramid_with_numbers(3)
```

**Explanation:**
- `def print_pyramid_with_numbers(n):` defines a function that takes an integer `n`.
- `num = 1` initializes the starting number.
- `for i in range(n):` iterates from 0 to `n-1`.
- `spaces = ' ' * (n - i - 1)` calculates the number of leading spaces.
- `numbers = ''.join(str(num + j) for j in range(2 * i + 1))` calculates the numbers.
- `print(spaces + numbers)` prints the spaces followed by numbers.
- `num += 2 * i + 1` increments the starting number for the next row.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printPyramidWithNumbers(int n) {
    int num = 1;  // Initialize the starting number
    for (int i = 0; i < n; i++) {  // Loop from 0 to n-1
        for (int j = 0; j < n - i - 1; j++) {  // Print leading spaces
            cout << " ";
        }
        for (int k = 0; k < 2 * i + 1; k++) {  // Print numbers
            cout << num + k;
        }
        num += 2 * i + 1;  // Increment the starting number for the next row
        cout << endl;  // Move to the next line after printing numbers
    }
}

int main() {
    printPyramidWithNumbers(3);  // Example usage
    return 0;
}
```

**Explanation:**
- `#include <iostream>` includes the input-output stream library.
- `using namespace std;` allows using standard library functions without the `std::` prefix.
- `void printPyramidWithNumbers(int n)` defines a function that takes an integer `n`.
- `int num = 1;` initializes the starting number.
- `for (int i = 0; i < n; i++)` iterates from 0 to `n-1`.
- `for (int j = 0; j < n - i - 1; j++)` prints leading spaces.
- `for (int k = 0; k < 2 * i + 1; k++)` prints numbers.
- `cout << num + k;` prints the current number.
- `num += 2 * i + 1;` increments the starting number for the next row.
- `cout << endl;` moves to the next line after printing numbers.

### Problem 11: Print a Pattern of Alternating 0s and 1s

**Python Code:**

```python
def print_alternating_pattern(n):
    for i in range(n):  # Loop from 0 to n-1
        for j in range(n):  # Loop from 0 to n-1
            print(1 if (i + j) % 2 == 0 else 0, end='')  # Print 1 if sum of indices is even, else 0
        print()  # Move to the next line after printing the row

# Example usage
print_alternating_pattern(4)
```

**Explanation:**
- `def print_alternating_pattern(n):` defines a function that takes an integer `n`.
- `for i in range(n):` iterates from 0 to `n-1` for rows.
- `for j in range(n):` iterates from 0 to `n-1` for columns.
- `print(1 if (i + j) % 2 == 0 else 0, end='')` prints 1 if the sum of indices is even, else 0.
- `print()` moves to the next line after printing the row.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printAlternatingPattern(int n) {
    for (int i = 0; i < n; i++) {  // Loop from 0 to n-1 for rows
        for (int j = 0; j < n; j++) {  // Loop from 0 to n-1 for columns
            cout << ((i + j) % 2 == 0 ? 1 : 0);  // Print 1 if sum of indices is even, else 0
        }
        cout << endl;  // Move to the next line after printing the row
    }
}

int main() {
    printAlternatingPattern(4);  // Example usage
    return 0;
}
```

**Explanation:**
- `#include <iostream>` includes the input-output stream library.
- `using namespace std;` allows using standard library functions without the `std::` prefix.
- `void printAlternatingPattern(int n)` defines a function that takes an integer `n`.
- `for (int i = 0; i < n; i++)` iterates from 0 to `n-1` for rows.
- `for (int j = 0; j < n; j++)` iterates from 0 to `n-1` for columns.
- `cout << ((i + j) % 2 == 0 ? 1 : 0);` prints 1 if the sum of indices is even, else 0.
- `cout << endl;` moves to the next line after printing the row.

### Problem 12: Print a Pascal’s Triangle

**Python Code:**

```python
def print_pascals_triangle(n):
    triangle = [[1]]  # Initialize the triangle with the first row
    for i in range(1, n):  # Loop from 1 to n-1
        row = [1]  # Start each row with 1
        for j in range(1, i):  # Loop from 1 to i-1
            row.append(triangle[i - 1][j - 1] + triangle[i - 1][j])  # Calculate the current element
        row.append(1)  # End each row with 1
        triangle.append(row)  # Add the row to the triangle
    for row in triangle:  # Print each row of the triangle
        print(' '.join(map(str, row)).center(2 * n))  # Center-align the row

# Example usage
print_pascals_triangle(4)
```

**Explanation:**
- `def print_pascals_triangle(n):` defines a function that takes an integer `n`.
- `triangle = [[1]]` initializes the triangle with the first row.
- `for i in range(1, n):` iterates from 1 to `n-1`.
- `row = [1]` starts each row with 1.
- `for j in range(1, i):` iterates from 1 to `i-1`.
- `row.append(triangle[i - 1][j - 1] + triangle[i - 1][j])` calculates the current element.
- `row.append(1)` ends each row with 1.
- `triangle.append(row)` adds the row to the triangle.
- `for row in triangle:` prints each row of the triangle.
- `print(' '.join(map(str, row)).center(2 * n))` center-aligns the row.

**C++ Code:**

```cpp
#include <iostream>
#include <vector>
using namespace std;

void printPascalsTriangle(int n) {
    vector<vector<int>> triangle = {{1}};  // Initialize the triangle with the first row
    for (int i = 1; i < n; i++) {  // Loop from 1 to n-1
        vector<int> row = {1};  // Start each row with 1
        for (int j = 1; j < i; j++) {  // Loop from 1 to i-1
            row.push_back(triangle[i - 1][j - 1] + triangle[i - 1][j]);  // Calculate the current element
        }
        row.push_back(1);  // End each row with 1
        triangle.push_back(row);  // Add the row to the triangle
    }
    for (const auto& row : triangle) {  // Print each row of the triangle
        for (int num : row) {
            cout << num << " ";
        }
        cout << endl;  // Move to the next line after printing the row
    }
}

int main() {
    printPascalsTriangle(4);  // Example usage
    return 0;
}
```

**Explanation:**
- `#include <iostream>` includes the input-output stream library.
- `#include <vector>` includes the vector library for dynamic arrays.
- `using namespace std;` allows using standard library functions without the `std::` prefix.
- `void printPascalsTriangle(int n)` defines a function that takes an integer `n`.
- `vector<vector<int>> triangle = {{1}};` initializes the triangle with the first row.
- `for (int i = 1; i < n; i++)` iterates from 1 to `n-1`.
- `vector<int> row = {1};` starts each row with 1.
- `for (int j = 1; j < i; j++)` iterates from 1 to `i-1`.
- `row.push_back(triangle[i - 1][j - 1] + triangle[i - 1][j]);` calculates the current element.
- `row.push_back(1);` ends each row with 1.
- `triangle.push_back(row);` adds the row to the triangle.
- `for (const auto& row : triangle)` prints each row of the triangle.
- `for (int num : row)` prints each number in the row.
- `cout << endl;` moves to the next line after printing the row.

### Problem 13: Print a Pattern of Consecutive Numbers

**Python Code:**

```python
def print_consecutive_numbers(n):
    num = 1  # Initialize the starting number
    for i in range(n):  # Loop from 0 to n-1
        row = []  # Initialize an empty row
        for j in range(n):  # Loop from 0 to n-1
            row.append(num)  # Add the current number to the row
            num += 1  # Increment the number
        print(' '.join(map(str, row)))  # Print the row with numbers separated by spaces

# Example usage
print_consecutive_numbers(3)
```

**Explanation:**
- `def print_consecutive_numbers(n):` defines a function that takes an integer `n`.
- `num = 1` initializes the starting number.
- `for i in range(n):` iterates from 0 to `n-1` for rows.
- `row = []` initializes an empty row.
- `for j in range(n):` iterates from 0 to `n-1` for columns.
- `row.append(num)` adds the current number to the row.
- `num += 1` increments the number.
- `print(' '.join(map(str, row)))` prints the row with numbers separated by spaces.

**C++ Code:**

```cpp
#include <iostream>
#include <vector>
using namespace std;

void printConsecutiveNumbers(int n) {
    int num = 1;  // Initialize the starting number
    for (int i = 0; i < n; i++) {  // Loop from 0 to n-1 for rows
        vector<int> row;  // Initialize an empty row
        for (int j = 0; j < n; j++) {  // Loop from 0 to n-1 for columns
            row.push_back(num);  // Add the current number to the row
            num += 1;  // Increment the number
        }
        for (int num : row) {  // Print the row with numbers separated by spaces
            cout << num << " ";
        }
        cout << endl;  // Move to the next line after printing the row
    }
}

int main() {
    printConsecutiveNumbers(3);  // Example usage
    return 0;
}
```

**Explanation:**
- `#include <iostream>` includes the input-output stream library.
- `#include <vector>` includes the vector library for dynamic arrays.
- `using namespace std;` allows using standard library functions without the `std::` prefix.
- `void printConsecutiveNumbers(int n)` defines a function that takes an integer `n`.
- `int num = 1;` initializes the starting number.
- `for (int i = 0; i < n; i++)` iterates from 0 to `n-1` for rows.
- `vector<int> row;` initializes an empty row.
- `for (int j = 0; j < n; j++)` iterates from 0 to `n-1` for columns.
- `row.push_back(num);` adds the current number to the row.
- `num += 1;` increments the number.
- `for (int num : row)` prints the row with numbers separated by spaces.
- `cout << endl;` moves to the next line after printing the row.

### Problem 14: Print a Star Pattern with Increasing Width

**Python Code:**

```python
def print_star_pattern_with_increasing_width(n):
    for i in range(n):  # Loop from 0 to n-1
        stars = '*' * (2 * i + 1)  # Calculate stars
        print(stars.center(2 * n - 1))  # Print stars centered horizontally

# Example usage
print_star_pattern_with_increasing_width(3)
```

**Explanation:**
- `def print_star_pattern_with_increasing_width(n):` defines a function that takes an integer `n`.
- `for i in range(n):` iterates from 0 to `n-1`.
- `stars = '*' * (2 * i + 1)` calculates the number of stars.
- `print(stars.center(2 * n - 1))` prints the stars centered horizontally.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printStarPatternWithIncreasingWidth(int n) {
    for (int i = 0; i < n; i++) {  // Loop from 0 to n-1
        for (int j = 0; j < n - i - 1; j++) {  // Print leading spaces
            cout << " ";
        }
        for (int k = 0; k < 2 * i + 1; k++) {  // Print stars
            cout << "*";
        }
        cout << endl;  // Move to the next line after printing stars
    }
}

int main() {
    printStarPatternWithIncreasingWidth(3);  // Example usage
    return 0;
}
```

**Explanation:**
- `#include <iostream>` includes the input-output stream library.
- `using namespace std;` allows using standard library functions without the `std::` prefix.
- `void printStarPatternWithIncreasingWidth(int n)` defines a function that takes an integer `n`.
- `for (int i = 0; i < n; i++)` iterates from 0 to `n-1`.
- `for (int j = 0; j < n - i - 1; j++)` prints leading spaces.
- `for (int k = 0; k < 2 * i + 1; k++)` prints stars.
- `cout << endl;` moves to the next line after printing stars.

### Problem 15: Print a Right-Angle Triangle Pattern with Characters

**Python Code:**

```python
def print_right_angle_triangle_with_characters(n):
    for i in range(n):  # Loop from 0 to n-1
        char = chr(ord('A') + i)  # Calculate the current character
        print(char * (i + 1))  # Print the character repeated i+1 times

# Example usage
print_right_angle_triangle_with_characters(3)
```

**Explanation:**
- `def print_right_angle_triangle_with_characters(n):` defines a function that takes an integer `n`.
- `for i in range(n):` iterates from 0 to `n-1`.
- `char = chr(ord('A') + i)` calculates the current character.
- `print(char * (i + 1))` prints the character repeated `i+1` times.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printRightAngleTriangleWithCharacters(int n) {
    for (int i = 0; i < n; i++) {  // Loop from 0 to n-1
        char ch = 'A' + i;  // Calculate the current character
        for (int j = 0; j <= i; j++) {  // Print the character repeated i+1 times
            cout << ch;
        }
        cout << endl;  // Move to the next line after printing characters
    }
}

int main() {
    printRightAngleTriangleWithCharacters(3);  // Example usage
    return 0;
}
```

**Explanation:**
- `#include <iostream>` includes the input-output stream library.
- `using namespace std;` allows using standard library functions without the `std::` prefix.
- `void printRightAngleTriangleWithCharacters(int n)` defines a function that takes an integer `n`.
- `for (int i = 0; i < n; i++)` iterates from 0 to `n-1`.
- `char ch = 'A' + i;` calculates the current character.
- `for (int j = 0; j <= i; j++)` prints the character repeated `i+1` times.
- `cout << endl;` moves to the next line after printing characters.

### Problem 16: Print a Checkerboard Pattern

**Python Code:**

```python
def print_checkerboard_pattern(n):
    for i in range(n):  # Loop from 0 to n-1
        for j in range(n):  # Loop from 0 to n-1
            print('X' if (i + j) % 2 == 0 else 'O', end='')  # Print 'X' if sum of indices is even, else 'O'
        print()  # Move to the next line after printing the row

# Example usage
print_checkerboard_pattern(4)
```

**Explanation:**
- `def print_checkerboard_pattern(n):` defines a function that takes an integer `n`.
- `for i in range(n):` iterates from 0 to `n-1` for rows.
- `for j in range(n):` iterates from 0 to `n-1` for columns.
- `print('X' if (i + j) % 2 == 0 else 'O', end='')` prints 'X' if the sum of indices is even, else 'O'.
- `print()` moves to the next line after printing the row.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printCheckerboardPattern(int n) {
    for (int i = 0; i < n; i++) {  // Loop from 0 to n-1 for rows
        for (int j = 0; j < n; j++) {  // Loop from 0 to n-1 for columns
            cout << ((i + j) % 2 == 0 ? 'X' : 'O');  // Print 'X' if sum of indices is even, else 'O'
        }
        cout << endl;  // Move to the next line after printing the row
    }
}

int main() {
    printCheckerboardPattern(4);  // Example usage
    return 0;
}
```

**Explanation:**
- `#include <iostream>` includes the input-output stream library.
- `using namespace std;` allows using standard library functions without the `std::` prefix.
- `void printCheckerboardPattern(int n)` defines a function that takes an integer `n`.
- `for (int i = 0; i < n; i++)` iterates from 0 to `n-1` for rows.
- `for (int j = 0; j < n; j++)` iterates from 0 to `n-1` for columns.
- `cout << ((i + j) % 2 == 0 ? 'X' : 'O');` prints 'X' if the sum of indices is even, else 'O'.
- `cout << endl;` moves to the next line after printing the row.

### Problem 17: Print a Pyramid Pattern of Increasing Stars

**Python Code:**

```python
def print_pyramid_of_increasing_stars(n):
    for i in range(n):  # Loop from 0 to n-1
        spaces = ' ' * (n - i - 1)  # Calculate leading spaces
        stars = '*' * (2 * i + 1)  # Calculate stars
        print(spaces + stars)  # Print spaces followed by stars

# Example usage
print_pyramid_of_increasing_stars(3)
```

**Explanation:**
- `def print_pyramid_of_increasing_stars(n):` defines a function that takes an integer `n`.
- `for i in range(n):` iterates from 0 to `n-1`.
- `spaces = ' ' * (n - i - 1)` calculates the number of leading spaces.
- `stars = '*' * (2 * i + 1)` calculates the number of stars.
- `print(spaces + stars)` prints the spaces followed by stars.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printPyramidOfIncreasingStars(int n) {
    for (int i = 0; i < n; i++) {  // Loop from 0 to n-1
        for (int j = 0; j < n - i - 1; j++) {  // Print leading spaces
            cout << " ";
        }
        for (int k = 0; k < 2 * i + 1; k++) {  // Print stars
            cout << "*";
        }
        cout << endl;  // Move to the next line after printing stars
    }
}

int main() {
    printPyramidOfIncreasingStars(3);  // Example usage
    return 0;
}
```

**Explanation:**
- `#include <iostream>` includes the input-output stream library.
- `using namespace std;` allows using standard library functions without the `std::` prefix.
- `void printPyramidOfIncreasingStars(int n)` defines a function that takes an integer `n`.
- `for (int i = 0; i < n; i++)` iterates from 0 to `n-1`.
- `for (int j = 0; j < n - i - 1; j++)` prints leading spaces.
- `for (int k = 0; k < 2 * i + 1; k++)` prints stars.
- `cout << endl;` moves to the next line after printing stars.

### Problem 18: Print a Border Pattern with Numbers

**Python Code:**

```python
def print_border_pattern_with_numbers(n):
    for i in range(n):  # Loop from 0 to n-1
        if i == 0 or i == n - 1:  # Print full row of numbers for the first and last rows
            print(''.join(str(j + 1) for j in range(n)))
        else:  # Print numbers at the borders and spaces in between
            print('1' + ' ' * (n - 2) + str(n))

# Example usage
print_border_pattern_with_numbers(4)
```

**Explanation:**
- `def print_border_pattern_with_numbers(n):` defines a function that takes an integer `n`.
- `for i in range(n):` iterates from 0 to `n-1`.
- `if i == 0 or i == n - 1:` checks if the current row is the first or last row.
- `print(''.join(str(j + 1) for j in range(n)))` prints a full row of numbers for the first and last rows.
- `else:` handles the rows in between.
- `print('1' + ' ' * (n - 2) + str(n))` prints numbers at the borders and spaces in between.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printBorderPatternWithNumbers(int n) {
    for (int i = 0; i < n; i++) {  // Loop from 0 to n-1
        if (i == 0 || i == n - 1) {  // Print full row of numbers for the first and last rows
            for (int j = 0; j < n; j++) {
                cout << j + 1;
            }
        } else {  // Print numbers at the borders and spaces in between
            cout << "1" << string(n - 2, ' ') << n;
        }
        cout << endl;  // Move to the next line after printing numbers
    }
}

int main() {
    printBorderPatternWithNumbers(4);  // Example usage
    return 0;
}
```

**Explanation:**
- `#include <iostream>` includes the input-output stream library.
- `using namespace std;` allows using standard library functions without the `std::` prefix.
- `void printBorderPatternWithNumbers(int n)` defines a function that takes an integer `n`.
- `for (int i = 0; i < n; i++)` iterates from 0 to `n-1`.
- `if (i == 0 || i == n - 1):` checks if the current row is the first or last row.
- `for (int j = 0; j < n; j++)` prints a full row of numbers for the first and last rows.
- `else:` handles the rows in between.
- `cout << "1" << string(n - 2, ' ') << n;` prints numbers at the borders and spaces in between.
- `cout << endl;` moves to the next line after printing numbers.

### Problem 19: Print an Inverted Pyramid Pattern with Characters

**Python Code:**

```python
def print_inverted_pyramid(n):
    # Loop through each row
    for i in range(n):
        # Print leading spaces
        for j in range(i):
            print(' ', end='')
        # Print characters
        for k in range(2 * (n - i) - 1):
            print(chr(65 + n - i - 1), end='')
        # Move to the next line
        print()

# Example usage
print_inverted_pyramid(3)
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The first inner loop prints leading spaces to center the characters.
  - The second inner loop prints the characters, decreasing the range with each row.
  - `chr(65 + n - i - 1)` converts the number to a character (A, B, C, etc.).
  - `print()` moves to the next line after each row is printed.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printInvertedPyramid(int n) {
    // Loop through each row
    for (int i = 0; i < n; i++) {
        // Print leading spaces
        for (int j = 0; j < i; j++) {
            cout << " ";
        }
        // Print characters
        for (int k = 0; k < 2 * (n - i) - 1; k++) {
            cout << char(65 + n - i - 1);
        }
        // Move to the next line
        cout << endl;
    }
}

int main() {
    printInvertedPyramid(3);
    return 0;
}
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The first inner loop prints leading spaces to center the characters.
  - The second inner loop prints the characters, decreasing the range with each row.
  - `char(65 + n - i - 1)` converts the number to a character (A, B, C, etc.).
  - `cout << endl;` moves to the next line after each row is printed.

### Problem 20: Print a Cross Pattern with Stars

**Python Code:**

```python
def print_cross_pattern(n):
    # Print the first row of stars
    print('*' * n)
    # Print the middle rows with a single star in the center
    for i in range(n - 2):
        print(' ' * (n // 2) + '*' + ' ' * (n // 2))
    # Print the last row of stars
    print('*' * n)

# Example usage
print_cross_pattern(5)
```

- **Explanation:**
  - The first `print` statement prints the top row of stars.
  - The loop prints the middle rows, each with a single star centered.
  - The last `print` statement prints the bottom row of stars.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printCrossPattern(int n) {
    // Print the first row of stars
    for (int i = 0; i < n; i++) {
        cout << "*";
    }
    cout << endl;
    // Print the middle rows with a single star in the center
    for (int i = 0; i < n - 2; i++) {
        for (int j = 0; j < n; j++) {
            if (j == n / 2) {
                cout << "*";
            } else {
                cout << " ";
            }
        }
        cout << endl;
    }
    // Print the last row of stars
    for (int i = 0; i < n; i++) {
        cout << "*";
    }
    cout << endl;
}

int main() {
    printCrossPattern(5);
    return 0;
}
```

- **Explanation:**
  - The first loop prints the top row of stars.
  - The nested loops print the middle rows, each with a single star centered.
  - The last loop prints the bottom row of stars.

### Problem 21: Print a Spiral Matrix

**Python Code:**

```python
def print_spiral_matrix(n):
    # Initialize the matrix with zeros
    matrix = [[0] * n for _ in range(n)]
    num = 1
    top, bottom, left, right = 0, n - 1, 0, n - 1

    while top <= bottom and left <= right:
        # Traverse from left to right
        for i in range(left, right + 1):
            matrix[top][i] = num
            num += 1
        top += 1
        # Traverse downwards
        for i in range(top, bottom + 1):
            matrix[i][right] = num
            num += 1
        right -= 1
        # Traverse from right to left
        for i in range(right, left - 1, -1):
            matrix[bottom][i] = num
            num += 1
        bottom -= 1
        # Traverse upwards
        for i in range(bottom, top - 1, -1):
            matrix[i][left] = num
            num += 1
        left += 1

    # Print the matrix
    for row in matrix:
        print(' '.join(map(str, row)))

# Example usage
print_spiral_matrix(3)
```

- **Explanation:**
  - Initialize a matrix with zeros.
  - Use four variables to track the boundaries of the spiral.
  - Fill the matrix in a spiral pattern by adjusting the boundaries.
  - Print the matrix row by row.

**C++ Code:**

```cpp
#include <iostream>
#include <vector>
using namespace std;

void printSpiralMatrix(int n) {
    // Initialize the matrix with zeros
    vector<vector<int>> matrix(n, vector<int>(n, 0));
    int num = 1;
    int top = 0, bottom = n - 1, left = 0, right = n - 1;

    while (top <= bottom && left <= right) {
        // Traverse from left to right
        for (int i = left; i <= right; i++) {
            matrix[top][i] = num++;
        }
        top++;
        // Traverse downwards
        for (int i = top; i <= bottom; i++) {
            matrix[i][right] = num++;
        }
        right--;
        // Traverse from right to left
        for (int i = right; i >= left; i--) {
            matrix[bottom][i] = num++;
        }
        bottom--;
        // Traverse upwards
        for (int i = bottom; i >= top; i--) {
            matrix[i][left] = num++;
        }
        left++;
    }

    // Print the matrix
    for (const auto& row : matrix) {
        for (int val : row) {
            cout << val << " ";
        }
        cout << endl;
    }
}

int main() {
    printSpiralMatrix(3);
    return 0;
}
```

- **Explanation:**
  - Initialize a matrix with zeros.
  - Use four variables to track the boundaries of the spiral.
  - Fill the matrix in a spiral pattern by adjusting the boundaries.
  - Print the matrix row by row.

### Problem 22: Print a Diamond Pattern with Increasing Width

**Python Code:**

```python
def print_diamond_pattern(n):
    # Print the upper part of the diamond
    for i in range(n):
        print(' ' * (n - i - 1) + '*' * (2 * i + 1))
    # Print the lower part of the diamond
    for i in range(n - 2, -1, -1):
        print(' ' * (n - i - 1) + '*' * (2 * i + 1))

# Example usage
print_diamond_pattern(3)
```

- **Explanation:**
  - The first loop prints the upper part of the diamond, increasing the width.
  - The second loop prints the lower part of the diamond, decreasing the width.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printDiamondPattern(int n) {
    // Print the upper part of the diamond
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n - i - 1; j++) {
            cout << " ";
        }
        for (int j = 0; j < 2 * i + 1; j++) {
            cout << "*";
        }
        cout << endl;
    }
    // Print the lower part of the diamond
    for (int i = n - 2; i >= 0; i--) {
        for (int j = 0; j < n - i - 1; j++) {
            cout << " ";
        }
        for (int j = 0; j < 2 * i + 1; j++) {
            cout << "*";
        }
        cout << endl;
    }
}

int main() {
    printDiamondPattern(3);
    return 0;
}
```

- **Explanation:**
  - The first nested loops print the upper part of the diamond, increasing the width.
  - The second nested loops print the lower part of the diamond, decreasing the width.

### Problem 23: Print a Diamond Pattern with Numbers Increasing

**Python Code:**

```python
def print_number_diamond_pattern(n):
    # Print the upper part of the diamond
    for i in range(n):
        # Print leading spaces
        print(' ' * (n - i - 1), end='')
        # Print increasing numbers
        for j in range(1, i + 2):
            print(j, end='')
        # Print decreasing numbers
        for j in range(i, 0, -1):
            print(j, end='')
        print()
    # Print the lower part of the diamond
    for i in range(n - 2, -1, -1):
        # Print leading spaces
        print(' ' * (n - i - 1), end='')
        # Print increasing numbers
        for j in range(1, i + 2):
            print(j, end='')
        # Print decreasing numbers
        for j in range(i, 0, -1):
            print(j, end='')
        print()

# Example usage
print_number_diamond_pattern(3)
```

- **Explanation:**
  - The first loop prints the upper part of the diamond, increasing the numbers.
  - The second loop prints the lower part of the diamond, decreasing the numbers.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printNumberDiamondPattern(int n) {
    // Print the upper part of the diamond
    for (int i = 0; i < n; i++) {
        // Print leading spaces
        for (int j = 0; j < n - i - 1; j++) {
            cout << " ";
        }
        // Print increasing numbers
        for (int j = 1; j <= i + 1; j++) {
            cout << j;
        }
        // Print decreasing numbers
        for (int j = i; j >= 1; j--) {
            cout << j;
        }
        cout << endl;
    }
    // Print the lower part of the diamond
    for (int i = n - 2; i >= 0; i--) {
        // Print leading spaces
        for (int j = 0; j < n - i - 1; j++) {
            cout << " ";
        }
        // Print increasing numbers
        for (int j = 1; j <= i + 1; j++) {
            cout << j;
        }
        // Print decreasing numbers
        for (int j = i; j >= 1; j--) {
            cout << j;
        }
        cout << endl;
    }
}

int main() {
    printNumberDiamondPattern(3);
    return 0;
}
```

- **Explanation:**
  - The first nested loops print the upper part of the diamond, increasing the numbers.
  - The second nested loops print the lower part of the diamond, decreasing the numbers.

### Problem 24: Print a Pattern of Increasing and Decreasing Stars

**Python Code:**

```python
def print_increasing_decreasing_stars(n):
    # Print the upper part of the pattern
    for i in range(n):
        print(' ' * (n - i - 1) + '*' * (2 * i + 1))
    # Print the lower part of the pattern
    for i in range(n - 2, -1, -1):
        print(' ' * (n - i - 1) + '*' * (2 * i + 1))

# Example usage
print_increasing_decreasing_stars(3)
```

- **Explanation:**
  - The first loop prints the upper part of the pattern, increasing the width.
  - The second loop prints the lower part of the pattern, decreasing the width.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printIncreasingDecreasingStars(int n) {
    // Print the upper part of the pattern
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n - i - 1; j++) {
            cout << " ";
        }
        for (int j = 0; j < 2 * i + 1; j++) {
            cout << "*";
        }
        cout << endl;
    }
    // Print the lower part of the pattern
    for (int i = n - 2; i >= 0; i--) {
        for (int j = 0; j < n - i - 1; j++) {
            cout << " ";
        }
        for (int j = 0; j < 2 * i + 1; j++) {
            cout << "*";
        }
        cout << endl;
    }
}

int main() {
    printIncreasingDecreasingStars(3);
    return 0;
}
```

- **Explanation:**
  - The first nested loops print the upper part of the pattern, increasing the width.
  - The second nested loops print the lower part of the pattern, decreasing the width.

### Problem 25: Print a Matrix with Zigzag Pattern

**Python Code:**

```python
def print_zigzag_matrix(n):
    # Initialize the matrix with zeros
    matrix = [[0] * n for _ in range(n)]
    num = 1

    for i in range(n):
        if i % 2 == 0:
            # Fill left to right
            for j in range(n):
                matrix[i][j] = num
                num += 1
        else:
            # Fill right to left
            for j in range(n - 1, -1, -1):
                matrix[i][j] = num
                num += 1

    # Print the matrix
    for row in matrix:
        print(' '.join(map(str, row)))

# Example usage
print_zigzag_matrix(3)
```

- **Explanation:**
  - Initialize a matrix with zeros.
  - Fill the matrix row by row, alternating directions based on the row index.
  - Print the matrix row by row.

**C++ Code:**

```cpp
#include <iostream>
#include <vector>
using namespace std;

void printZigzagMatrix(int n) {
    // Initialize the matrix with zeros
    vector<vector<int>> matrix(n, vector<int>(n, 0));
    int num = 1;

    for (int i = 0; i < n; i++) {
        if (i % 2 == 0) {
            // Fill left to right
            for (int j = 0; j < n; j++) {
                matrix[i][j] = num++;
            }
        } else {
            // Fill right to left
            for (int j = n - 1; j >= 0; j--) {
                matrix[i][j] = num++;
            }
        }
    }

    // Print the matrix
    for (const auto& row : matrix) {
        for (int val : row) {
            cout << val << " ";
        }
        cout << endl;
    }
}

int main() {
    printZigzagMatrix(3);
    return 0;
}
```

- **Explanation:**
  - Initialize a matrix with zeros.
  - Fill the matrix row by row, alternating directions based on the row index.
  - Print the matrix row by row.

### Problem 26: Print a Pattern of Alternating Characters in Rows

**Python Code:**

```python
def print_alternating_characters(n):
    for i in range(n):
        for j in range(n):
            if (i + j) % 2 == 0:
                print('A', end='')
            else:
                print('B', end='')
        print()

# Example usage
print_alternating_characters(4)
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The inner loop iterates over each column.
  - Print 'A' if the sum of the indices is even, otherwise print 'B'.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printAlternatingCharacters(int n) {
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            if ((i + j) % 2 == 0) {
                cout << "A";
            } else {
                cout << "B";
            }
        }
        cout << endl;
    }
}

int main() {
    printAlternatingCharacters(4);
    return 0;
}
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The inner loop iterates over each column.
  - Print 'A' if the sum of the indices is even, otherwise print 'B'.

### Problem 27: Print a Number Pyramid Pattern with Characters

**Python Code:**

```python
def print_number_pyramid(n):
    num = 1
    for i in range(n):
        # Print leading spaces
        print(' ' * (n - i - 1), end='')
        # Print characters
        for j in range(2 * i + 1):
            print(chr(64 + num), end='')
            num += 1
        print()

# Example usage
print_number_pyramid(3)
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The first `print` statement prints leading spaces.
  - The inner loop prints characters, converting numbers to characters.
  - `print()` moves to the next line after each row is printed.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printNumberPyramid(int n) {
    int num = 1;
    for (int i = 0; i < n; i++) {
        // Print leading spaces
        for (int j = 0; j < n - i - 1; j++) {
            cout << " ";
        }
        // Print characters
        for (int j = 0; j < 2 * i + 1; j++) {
            cout << char(64 + num);
            num++;
        }
        cout << endl;
    }
}

int main() {
    printNumberPyramid(3);
    return 0;
}
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The first inner loop prints leading spaces.
  - The second inner loop prints characters, converting numbers to characters.
  - `cout << endl;` moves to the next line after each row is printed.

### Problem 28: Print a Pattern with Diagonal Lines

**Python Code:**

```python
def print_diagonal_pattern(n):
    for i in range(n):
        for j in range(n):
            if i == j:
                print(chr(65 + i), end='')
            else:
                print(' ', end='')
        print()

# Example usage
print_diagonal_pattern(4)
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The inner loop iterates over each column.
  - Print the character if the row index equals the column index, otherwise print a space.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printDiagonalPattern(int n) {
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            if (i == j) {
                cout << char(65 + i);
            } else {
                cout << " ";
            }
        }
        cout << endl;
    }
}

int main() {
    printDiagonalPattern(4);
    return 0;
}
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The inner loop iterates over each column.
  - Print the character if the row index equals the column index, otherwise print a space.

### Problem 29: Print a Matrix with Diamond Pattern of Numbers

**Python Code:**

```python
def print_diamond_number_matrix(n):
    # Initialize the matrix with zeros
    matrix = [[0] * (2 * n - 1) for _ in range(n)]
    num = 1

    for i in range(n):
        for j in range(n - i - 1, n + i):
            matrix[i][j] = num
            num += 1

    for i in range(n - 2, -1, -1):
        for j in range(n - i - 1, n + i):
            matrix[i][j] = num
            num += 1

    # Print the matrix
    for row in matrix:
        print(' '.join(map(str, row)))

# Example usage
print_diamond_number_matrix(3)
```

- **Explanation:**
  - Initialize a matrix with zeros.
  - Fill the upper part of the diamond pattern.
  - Fill the lower part of the diamond pattern.
  - Print the matrix row by row.

**C++ Code:**

```cpp
#include <iostream>
#include <vector>
using namespace std;

void printDiamondNumberMatrix(int n) {
    // Initialize the matrix with zeros
    vector<vector<int>> matrix(n, vector<int>(2 * n - 1, 0));
    int num = 1;

    for (int i = 0; i < n; i++) {
        for (int j = n - i - 1; j < n + i; j++) {
            matrix[i][j] = num++;
        }
    }

    for (int i = n - 2; i >= 0; i--) {
        for (int j = n - i - 1; j < n + i; j++) {
            matrix[i][j] = num++;
        }
    }

    // Print the matrix
    for (const auto& row : matrix) {
        for (int val : row) {
            cout << val << " ";
        }
        cout << endl;
    }
}

int main() {
    printDiamondNumberMatrix(3);
    return 0;
}
```

- **Explanation:**
  - Initialize a matrix with zeros.
  - Fill the upper part of the diamond pattern.
  - Fill the lower part of the diamond pattern.
  - Print the matrix row by row.

### Problem 30: Print a Cross Pattern of Stars with Diagonals

**Python Code:**

```python
def print_cross_with_diagonals(n):
    for i in range(n):
        for j in range(n):
            if i == j or i == n - j - 1 or i == n // 2 or j == n // 2:
                print('*', end='')
            else:
                print(' ', end='')
        print()

# Example usage
print_cross_with_diagonals(5)
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The inner loop iterates over each column.
  - Print a star if the indices match the cross or diagonal pattern, otherwise print a space.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printCrossWithDiagonals(int n) {
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            if (i == j || i == n - j - 1 || i == n / 2 || j == n / 2) {
                cout << "*";
            } else {
                cout << " ";
            }
        }
        cout << endl;
    }
}

int main() {
    printCrossWithDiagonals(5);
    return 0;
}
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The inner loop iterates over each column.
  - Print a star if the indices match the cross or diagonal pattern, otherwise print a space.

### Problem 31: Print a Triangular Matrix with Numbers

**Python Code:**

```python
def print_triangular_matrix(n):
    num = 1
    for i in range(n):
        for j in range(i + 1):
            print(num, end=' ')
            num += 1
        print()

# Example usage
print_triangular_matrix(3)
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The inner loop iterates over each column in the row.
  - Print the number and increment it.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printTriangularMatrix(int n) {
    int num = 1;
    for (int i = 0; i < n; i++) {
        for (int j = 0; j <= i; j++) {
            cout << num << " ";
            num++;
        }
        cout << endl;
    }
}

int main() {
    printTriangularMatrix(3);
    return 0;
}
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The inner loop iterates over each column in the row.
  - Print the number and increment it.

### Problem 32: Print a Star Pattern with Increasing and Decreasing Width

**Python Code:**

```python
def print_star_pattern(n):
    # Print the upper part of the pattern
    for i in range(n):
        print(' ' * (n - i - 1) + '*' * (2 * i + 1))
    # Print the lower part of the pattern
    for i in range(n - 2, -1, -1):
        print(' ' * (n - i - 1) + '*' * (2 * i + 1))

# Example usage
print_star_pattern(3)
```

- **Explanation:**
  - The first loop prints the upper part of the pattern, increasing the width.
  - The second loop prints the lower part of the pattern, decreasing the width.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printStarPattern(int n) {
    // Print the upper part of the pattern
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n - i - 1; j++) {
            cout << " ";
        }
        for (int j = 0; j < 2 * i + 1; j++) {
            cout << "*";
        }
        cout << endl;
    }
    // Print the lower part of the pattern
    for (int i = n - 2; i >= 0; i--) {
        for (int j = 0; j < n - i - 1; j++) {
            cout << " ";
        }
        for (int j = 0; j < 2 * i + 1; j++) {
            cout << "*";
        }
        cout << endl;
    }
}

int main() {
    printStarPattern(3);
    return 0;
}
```

- **Explanation:**
  - The first nested loops print the upper part of the pattern, increasing the width.
  - The second nested loops print the lower part of the pattern, decreasing the width.

### Problem 33: Print a Pattern of Nested Squares

**Python Code:**

```python
def print_nested_squares(n):
    for i in range(n):
        for j in range(n):
            if i == 0 or i == n - 1 or j == 0 or j == n - 1:
                print('*', end='')
            elif i == j or i == n - j - 1:
                print('*', end='')
            else:
                print(' ', end='')
        print()

# Example usage
print_nested_squares(5)
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The inner loop iterates over each column.
  - Print a star if the indices match the outer square or the diagonals, otherwise print a space.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printNestedSquares(int n) {
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            if (i == 0 || i == n - 1 || j == 0 || j == n - 1) {
                cout << "*";
            } else if (i == j || i == n - j - 1) {
                cout << "*";
            } else {
                cout << " ";
            }
        }
        cout << endl;
    }
}

int main() {
    printNestedSquares(5);
    return 0;
}
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The inner loop iterates over each column.
  - Print a star if the indices match the outer square or the diagonals, otherwise print a space.

### Problem 34: Print a Pattern with Increasing Characters in Columns

**Python Code:**

```python
def print_increasing_columns(n):
    num = 1
    for i in range(n):
        for j in range(i + 1):
            print(chr(64 + num), end=' ')
            num += 1
        print()

# Example usage
print_increasing_columns(3)
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The inner loop iterates over each column in the row.
  - Print the character and increment the number.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printIncreasingColumns(int n) {
    int num = 1;
    for (int i = 0; i < n; i++) {
        for (int j = 0; j <= i; j++) {
            cout << char(64 + num) << " ";
            num++;
        }
        cout << endl;
    }
}

int main() {
    printIncreasingColumns(3);
    return 0;
}
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The inner loop iterates over each column in the row.
  - Print the character and increment the number.

### Problem 35: Print a Matrix with Spiral Diagonals

**Python Code:**

```python
def print_spiral_diagonal_matrix(n):
    # Initialize the matrix with zeros
    matrix = [[0] * n for _ in range(n)]
    num = 1
    row, col = 0, 0

    for layer in range(n):
        # Move right
        while col < n and matrix[row][col] == 0:
            matrix[row][col] = num
            num += 1
            col += 1
        col -= 1
        row += 1
        # Move down
        while row < n and matrix[row][col] == 0:
            matrix[row][col] = num
            num += 1
            row += 1
        row -= 1
        col -= 1
        # Move left
        while col >= 0 and matrix[row][col] == 0:
            matrix[row][col] = num
            num += 1
            col -= 1
        col += 1
        row -= 1
        # Move up
        while row >= 0 and matrix[row][col] == 0:
            matrix[row][col] = num
            num += 1
            row -= 1
        row += 1
        col += 1

    # Print the matrix
    for row in matrix:
        print(' '.join(map(str, row)))

# Example usage
print_spiral_diagonal_matrix(3)
```

- **Explanation:**
  - Initialize a matrix with zeros.
  - Use a loop to fill the matrix in a spiral diagonal pattern.
  - Print the matrix row by row.

**C++ Code:**

```cpp
#include <iostream>
#include <vector>
using namespace std;

void printSpiralDiagonalMatrix(int n) {
    // Initialize the matrix with zeros
    vector<vector<int>> matrix(n, vector<int>(n, 0));
    int num = 1;
    int row = 0, col = 0;

    for (int layer = 0; layer < n; layer++) {
        // Move right
        while (col < n && matrix[row][col] == 0) {
            matrix[row][col] = num++;
            col++;
        }
        col--;
        row++;
        // Move down
        while (row < n && matrix[row][col] == 0) {
            matrix[row][col] = num++;
            row++;
        }
        row--;
        col--;
        // Move left
        while (col >= 0 && matrix[row][col] == 0) {
            matrix[row][col] = num++;
            col--;
        }
        col++;
        row--;
        // Move up
        while (row >= 0 && matrix[row][col] == 0) {
            matrix[row][col] = num++;
            row--;
        }
        row++;
        col++;
    }

    // Print the matrix
    for (const auto& row : matrix) {
        for (int val : row) {
            cout << val << " ";
        }
        cout << endl;
    }
}

int main() {
    printSpiralDiagonalMatrix(3);
    return 0;
}
```

- **Explanation:**
  - Initialize a matrix with zeros.
  - Use a loop to fill the matrix in a spiral diagonal pattern.
  - Print the matrix row by row.

### Problem 36: Print a Checkerboard Pattern with Increasing Size

**Python Code:**

```python
def print_checkerboard_pattern(n):
    for i in range(n):
        for j in range(n):
            if (i + j) % 2 == 0:
                print('X', end='')
            else:
                print('O', end='')
        print()

# Example usage
print_checkerboard_pattern(3)
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The inner loop iterates over each column.
  - Print 'X' if the sum of the indices is even, otherwise print 'O'.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printCheckerboardPattern(int n) {
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            if ((i + j) % 2 == 0) {
                cout << "X";
            } else {
                cout << "O";
            }
        }
        cout << endl;
    }
}

int main() {
    printCheckerboardPattern(3);
    return 0;
}
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The inner loop iterates over each column.
  - Print 'X' if the sum of the indices is even, otherwise print 'O'.

### Problem 37: Print a Cross Pattern with Increasing Size

**Python Code:**

```python
def print_increasing_cross_pattern(n):
    # Print the upper part of the cross
    for i in range(n):
        print(' ' * (n - i - 1) + '*' * (2 * i + 1))
    # Print the lower part of the cross
    for i in range(n - 2, -1, -1):
        print(' ' * (n - i - 1) + '*' * (2 * i + 1))

# Example usage
print_increasing_cross_pattern(3)
```

- **Explanation:**
  - The first loop prints the upper part of the cross, increasing the width.
  - The second loop prints the lower part of the cross, decreasing the width.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printIncreasingCrossPattern(int n) {
    // Print the upper part of the cross
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n - i - 1; j++) {
            cout << " ";
        }
        for (int j = 0; j < 2 * i + 1; j++) {
            cout << "*";
        }
        cout << endl;
    }
    // Print the lower part of the cross
    for (int i = n - 2; i >= 0; i--) {
        for (int j = 0; j < n - i - 1; j++) {
            cout << " ";
        }
        for (int j = 0; j < 2 * i + 1; j++) {
            cout << "*";
        }
        cout << endl;
    }
}

int main() {
    printIncreasingCrossPattern(3);
    return 0;
}
```

- **Explanation:**
  - The first nested loops print the upper part of the cross, increasing the width.
  - The second nested loops print the lower part of the cross, decreasing the width.

### Problem 38: Print a Pattern of Alternating Triangles

**Python Code:**

```python
def print_alternating_triangles(n):
    for i in range(n):
        if i % 2 == 0:
            # Print increasing stars
            print(' ' * (n - i - 1) + '*' * (2 * i + 1))
        else:
            # Print decreasing stars
            print(' ' * i + '*' * (2 * (n - i) - 1))

# Example usage
print_alternating_triangles(3)
```

- **Explanation:**
  - The loop iterates over each row.
  - Print increasing stars if the row index is even, otherwise print decreasing stars.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printAlternatingTriangles(int n) {
    for (int i = 0; i < n; i++) {
        if (i % 2 == 0) {
            // Print increasing stars
            for (int j = 0; j < n - i - 1; j++) {
                cout << " ";
            }
            for (int j = 0; j < 2 * i + 1; j++) {
                cout << "*";
            }
        } else {
            // Print decreasing stars
            for (int j = 0; j < i; j++) {
                cout << " ";
            }
            for (int j = 0; j < 2 * (n - i) - 1; j++) {
                cout << "*";
            }
        }
        cout << endl;
    }
}

int main() {
    printAlternatingTriangles(3);
    return 0;
}
```

- **Explanation:**
  - The loop iterates over each row.
  - Print increasing stars if the row index is even, otherwise print decreasing stars.

### Problem 39: Print a Matrix with Diamond Pattern of Numbers

**Python Code:**

```python
def print_diamond_number_pattern(n):
    # Initialize the matrix with zeros
    matrix = [[0] * (2 * n - 1) for _ in range(n)]
    num = 1

    for i in range(n):
        for j in range(n - i - 1, n + i):
            matrix[i][j] = num
            num += 1

    for i in range(n - 2, -1, -1):
        for j in range(n - i - 1, n + i):
            matrix[i][j] = num
            num += 1

    # Print the matrix
    for row in matrix:
        print(' '.join(map(str, row)))

# Example usage
print_diamond_number_pattern(3)
```

- **Explanation:**
  - Initialize a matrix with zeros.
  - Fill the upper part of the diamond pattern.
  - Fill the lower part of the diamond pattern.
  - Print the matrix row by row.

**C++ Code:**

```cpp
#include <iostream>
#include <vector>
using namespace std;

void printDiamondNumberPattern(int n) {
    // Initialize the matrix with zeros
    vector<vector<int>> matrix(n, vector<int>(2 * n - 1, 0));
    int num = 1;

    for (int i = 0; i < n; i++) {
        for (int j = n - i - 1; j < n + i; j++) {
            matrix[i][j] = num++;
        }
    }

    for (int i = n - 2; i >= 0; i--) {
        for (int j = n - i - 1; j < n + i; j++) {
            matrix[i][j] = num++;
        }
    }

    // Print the matrix
    for (const auto& row : matrix) {
        for (int val : row) {
            cout << val << " ";
        }
        cout << endl;
    }
}

int main() {
    printDiamondNumberPattern(3);
    return 0;
}
```

- **Explanation:**
  - Initialize a matrix with zeros.
  - Fill the upper part of the diamond pattern.
  - Fill the lower part of the diamond pattern.
  - Print the matrix row by row.

### Problem 40: Print a Star Pattern with Increasing Width and Centered

**Python Code:**

```python
def print_centered_star_pattern(n):
    for i in range(n):
        print(' ' * (n - i - 1) + '*' * (2 * i + 1))

# Example usage
print_centered_star_pattern(3)
```

- **Explanation:**
  - The loop iterates over each row.
  - Print leading spaces and stars, increasing the width with each row.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printCenteredStarPattern(int n) {
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n - i - 1; j++) {
            cout << " ";
        }
        for (int j = 0; j < 2 * i + 1; j++) {
            cout << "*";
        }
        cout << endl;
    }
}

int main() {
    printCenteredStarPattern(3);
    return 0;
}
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The first inner loop prints leading spaces.
  - The second inner loop prints stars, increasing the width with each row.

### Problem 41: Print a Pattern with Spiral and Zigzag

**Python Code:**

```python
def print_spiral_zigzag_pattern(n):
    # Initialize the matrix with zeros
    matrix = [[0] * n for _ in range(n)]
    num = 1
    top, bottom, left, right = 0, n - 1, 0, n - 1

    while top <= bottom and left <= right:
        # Traverse from left to right
        for i in range(left, right + 1):
            matrix[top][i] = num
            num += 1
        top += 1
        # Traverse downwards
        for i in range(top, bottom + 1):
            matrix[i][right] = num
            num += 1
        right -= 1
        # Traverse from right to left
        for i in range(right, left - 1, -1):
            matrix[bottom][i] = num
            num += 1
        bottom -= 1
        # Traverse upwards
        for i in range(bottom, top - 1, -1):
            matrix[i][left] = num
            num += 1
        left += 1

    # Fill the remaining cells in zigzag pattern
    for i in range(n):
        if i % 2 == 0:
            for j in range(n):
                if matrix[i][j] == 0:
                    matrix[i][j] = num
                    num += 1
        else:
            for j in range(n - 1, -1, -1):
                if matrix[i][j] == 0:
                    matrix[i][j] = num
                    num += 1

    # Print the matrix
    for row in matrix:
        print(' '.join(map(str, row)))

# Example usage
print_spiral_zigzag_pattern(3)
```

- **Explanation:**
  - Initialize a matrix with zeros.
  - Fill the matrix in a spiral pattern.
  - Fill the remaining cells in a zigzag pattern.
  - Print the matrix row by row.

**C++ Code:**

```cpp
#include <iostream>
#include <vector>
using namespace std;

void printSpiralZigzagPattern(int n) {
    // Initialize the matrix with zeros
    vector<vector<int>> matrix(n, vector<int>(n, 0));
    int num = 1;
    int top = 0, bottom = n - 1, left = 0, right = n - 1;

    while (top <= bottom && left <= right) {
        // Traverse from left to right
        for (int i = left; i <= right; i++) {
            matrix[top][i] = num++;
        }
        top++;
        // Traverse downwards
        for (int i = top; i <= bottom; i++) {
            matrix[i][right] = num++;
        }
        right--;
        // Traverse from right to left
        for (int i = right; i >= left; i--) {
            matrix[bottom][i] = num++;
        }
        bottom--;
        // Traverse upwards
        for (int i = bottom; i >= top; i--) {
            matrix[i][left] = num++;
        }
        left++;
    }

    // Fill the remaining cells in zigzag pattern
    for (int i = 0; i < n; i++) {
        if (i % 2 == 0) {
            for (int j = 0; j < n; j++) {
                if (matrix[i][j] == 0) {
                    matrix[i][j] = num++;
                }
            }
        } else {
            for (int j = n - 1; j >= 0; j--) {
                if (matrix[i][j] == 0) {
                    matrix[i][j] = num++;
                }
            }
        }
    }

    // Print the matrix
    for (const auto& row : matrix) {
        for (int val : row) {
            cout << val << " ";
        }
        cout << endl;
    }
}

int main() {
    printSpiralZigzagPattern(3);
    return 0;
}
```

- **Explanation:**
  - Initialize a matrix with zeros.
  - Fill the matrix in a spiral pattern.
  - Fill the remaining cells in a zigzag pattern.
  - Print the matrix row by row.

### Problem 42: Print a Pattern of Alternating Characters in Matrix

**Python Code:**

```python
def print_alternating_matrix(n):
    for i in range(n):
        for j in range(n):
            if (i + j) % 2 == 0:
                print('A', end='')
            else:
                print('B', end='')
        print()

# Example usage
print_alternating_matrix(3)
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The inner loop iterates over each column.
  - Print 'A' if the sum of the indices is even, otherwise print 'B'.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printAlternatingMatrix(int n) {
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            if ((i + j) % 2 == 0) {
                cout << "A";
            } else {
                cout << "B";
            }
        }
        cout << endl;
    }
}

int main() {
    printAlternatingMatrix(3);
    return 0;
}
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The inner loop iterates over each column.
  - Print 'A' if the sum of the indices is even, otherwise print 'B'.

### Problem 43: Print a Pattern with Nested Triangles

**Python Code:**

```python
def print_nested_triangles(n):
    for i in range(n):
        print(' ' * (n - i - 1) + '*' * (2 * i + 1))
    for i in range(n - 2, -1, -1):
        print(' ' * (n - i - 1) + '*' * (2 * i + 1))

# Example usage
print_nested_triangles(3)
```

- **Explanation:**
  - The first loop prints the upper part of the pattern, increasing the width.
  - The second loop prints the lower part of the pattern, decreasing the width.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printNestedTriangles(int n) {
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n - i - 1; j++) {
            cout << " ";
        }
        for (int j = 0; j < 2 * i + 1; j++) {
            cout << "*";
        }
        cout << endl;
    }
    for (int i = n - 2; i >= 0; i--) {
        for (int j = 0; j < n - i - 1; j++) {
            cout << " ";
        }
        for (int j = 0; j < 2 * i + 1; j++) {
            cout << "*";
        }
        cout << endl;
    }
}

int main() {
    printNestedTriangles(3);
    return 0;
}
```

- **Explanation:**
  - The first nested loops print the upper part of the pattern, increasing the width.
  - The second nested loops print the lower part of the pattern, decreasing the width.

### Problem 44: Print a Matrix with Increasing Rows and Columns

**Python Code:**

```python
def print_increasing_matrix(n):
    num = 1
    for i in range(n):
        for j in range(n):
            print(num, end=' ')
            num += 1
        print()

# Example usage
print_increasing_matrix(3)
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The inner loop iterates over each column.
  - Print the number and increment it.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printIncreasingMatrix(int n) {
    int num = 1;
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            cout << num << " ";
            num++;
        }
        cout << endl;
    }
}

int main() {
    printIncreasingMatrix(3);
    return 0;
}
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The inner loop iterates over each column.
  - Print the number and increment it.

### Problem 45: Print a Pattern with Rows of Increasing Characters

**Python Code:**

```python
def print_increasing_rows(n):
    num = 1
    for i in range(n):
        for j in range(i + 1):
            print(chr(64 + num), end='')
            num += 1
        print()

# Example usage
print_increasing_rows(3)
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The inner loop iterates over each column in the row.
  - Print the character and increment the number.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printIncreasingRows(int n) {
    int num = 1;
    for (int i = 0; i < n; i++) {
        for (int j = 0; j <= i; j++) {
            cout << char(64 + num);
            num++;
        }
        cout << endl;
    }
}

int main() {
    printIncreasingRows(3);
    return 0;
}
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The inner loop iterates over each column in the row.
  - Print the character and increment the number.

### Problem 46: Print a Star Pattern with Diamond Shape and Numbers

**Python Code:**

```python
def print_diamond_star_pattern(n):
    num = 1
    # Print the upper part of the diamond
    for i in range(n):
        print(' ' * (n - i - 1), end='')
        for j in range(2 * i + 1):
            print(num, end='')
            num += 1
        print()
    # Print the lower part of the diamond
    for i in range(n - 2, -1, -1):
        print(' ' * (n - i - 1), end='')
        for j in range(2 * i + 1):
            print(num, end='')
            num += 1
        print()

# Example usage
print_diamond_star_pattern(3)
```

- **Explanation:**
  - The first loop prints the upper part of the diamond, increasing the width.
  - The second loop prints the lower part of the diamond, decreasing the width.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printDiamondStarPattern(int n) {
    int num = 1;
    // Print the upper part of the diamond
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n - i - 1; j++) {
            cout << " ";
        }
        for (int j = 0; j < 2 * i + 1; j++) {
            cout << num;
            num++;
        }
        cout << endl;
    }
    // Print the lower part of the diamond
    for (int i = n - 2; i >= 0; i--) {
        for (int j = 0; j < n - i - 1; j++) {
            cout << " ";
        }
        for (int j = 0; j < 2 * i + 1; j++) {
            cout << num;
            num++;
        }
        cout << endl;
    }
}

int main() {
    printDiamondStarPattern(3);
    return 0;
}
```

- **Explanation:**
  - The first nested loops print the upper part of the diamond, increasing the width.
  - The second nested loops print the lower part of the diamond, decreasing the width.

### Problem 47: Print a Matrix with Cross Pattern of Numbers

**Python Code:**

```python
def print_cross_number_matrix(n):
    # Initialize the matrix with zeros
    matrix = [[0] * n for _ in range(n)]
    num = 1

    for i in range(n):
        for j in range(n):
            if i == n // 2 or j == n // 2 or i == j or i == n - j - 1:
                matrix[i][j] = num
                num += 1

    # Print the matrix
    for row in matrix:
        print(' '.join(map(str, row)))

# Example usage
print_cross_number_matrix(5)
```

- **Explanation:**
  - Initialize a matrix with zeros.
  - Fill the matrix with numbers in a cross pattern.
  - Print the matrix row by row.

**C++ Code:**

```cpp
#include <iostream>
#include <vector>
using namespace std;

void printCrossNumberMatrix(int n) {
    // Initialize the matrix with zeros
    vector<vector<int>> matrix(n, vector<int>(n, 0));
    int num = 1;

    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            if (i == n / 2 || j == n / 2 || i == j || i == n - j - 1) {
                matrix[i][j] = num++;
            }
        }
    }

    // Print the matrix
    for (const auto& row : matrix) {
        for (int val : row) {
            cout << val << " ";
        }
        cout << endl;
    }
}

int main() {
    printCrossNumberMatrix(5);
    return 0;
}
```

- **Explanation:**
  - Initialize a matrix with zeros.
  - Fill the matrix with numbers in a cross pattern.
  - Print the matrix row by row.

### Problem 48: Print a Pattern with Concentric Squares

**Python Code:**

```python
def print_concentric_squares(n):
    for i in range(n):
        for j in range(n):
            if i == 0 or i == n - 1 or j == 0 or j == n - 1:
                print('*', end='')
            else:
                print(' ', end='')
        print()

# Example usage
print_concentric_squares(5)
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The inner loop iterates over each column.
  - Print a star if the indices match the outer square, otherwise print a space.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printConcentricSquares(int n) {
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            if (i == 0 || i == n - 1 || j == 0 || j == n - 1) {
                cout << "*";
            } else {
                cout << " ";
            }
        }
        cout << endl;
    }
}

int main() {
    printConcentricSquares(5);
    return 0;
}
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The inner loop iterates over each column.
  - Print a star if the indices match the outer square, otherwise print a space.

### Problem 49: Print a Pattern with Alternating Rows and Columns of Numbers

**Python Code:**

```python
def print_alternating_numbers(n):
    num = 1
    for i in range(n):
        for j in range(n):
            print(num, end=' ')
            num += 1
        print()

# Example usage
print_alternating_numbers(3)
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The inner loop iterates over each column.
  - Print the number and increment it.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printAlternatingNumbers(int n) {
    int num = 1;
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            cout << num << " ";
            num++;
        }
        cout << endl;
    }
}

int main() {
    printAlternatingNumbers(3);
    return 0;
}
```

- **Explanation:**
  - The outer loop iterates over each row.
  - The inner loop iterates over each column.
  - Print the number and increment it.

### Problem 50: Print a Matrix with Zigzag Pattern of Stars

**Python Code:**

```python
def print_zigzag_star_matrix(n):
    for i in range(n):
        if i % 2 == 0:
            print('* ' * n)
        else:
            print(' *' * n)

# Example usage
print_zigzag_star_matrix(3)
```

- **Explanation:**
  - The loop iterates over each row.
  - Print stars with alternating patterns based on the row index.

**C++ Code:**

```cpp
#include <iostream>
using namespace std;

void printZigzagStarMatrix(int n) {
    for (int i = 0; i < n; i++) {
        if (i % 2 == 0) {
            for (int j = 0; j < n; j++) {
                cout << "* ";
            }
        } else {
            for (int j = 0; j < n; j++) {
                cout << " *";
            }
        }
        cout << endl;
    }
}

int main() {
    printZigzagStarMatrix(3);
    return 0;
}
```

- **Explanation:**
  - The loop iterates over each row.
  - Print stars with alternating patterns based on the row index.