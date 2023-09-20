## Homework Question for Functions & Some Problem Statements
1) Can we create more than one main function in a single program?
2) Can we return 1,-1 in the main() function?
3) Why no input paramters inside main()? Can we put input parameters inside main() function?
4) Can we write any expression inside the case of switch statement? 
5) Function to display area of circle
6) Number is odd or even
7) Factorial of number
8) Number is prime or not
9) Print all prime numbers from 1 to n
10) Why can't we calculate factorial above 13?
11) Reverse an integer
12) Set the ith bit
13) Convert celsius to fahrenheit.


## Homework Question Answer for Functions & Some Problem Statements

1) Can we create more than one main function in a single program?
- No, you can only have one `main` function in a C++ program.

```cpp
int main() {
    // Your code here
    return 0;
}
```

2) Can we return 1,-1 in the main() function?
- Yes, you can return 1 or -1 from `main()` to indicate that the program ended with an error.

```cpp
int main() {
    // Your code here

    // Indicate an error
    return -1;
}
```

3) Why no input paramters inside main()? Can we put input parameters inside main() function?
- In C++, `main` is defined to take no parameters by default. However, you can use command line arguments to pass values to your program.

```cpp
int main(int argc, char* argv[]) {
    // argc is the number of arguments passed (including the program name)
    // argv is an array of C-style strings containing the arguments

    // Your code here

    return 0;
}
```

4) Can we write any expression inside the case of switch statement?
- Yes, you can write any expression inside a `case` label in a switch statement.

```cpp
int number = 3;
switch(number) {
    case 1:
        // Code for case 1
        break;
    case 2:
        // Code for case 2
        break;
    default:
        // Default case
        break;
}
```

5) Function to display area of circle

```cpp
#include <iostream>
using namespace std;

const double PI = 3.14159;

double calculateArea(double radius) {
    return PI * radius * radius;
}

int main() {
    double radius = 5.0;
    double area = calculateArea(radius);
    cout << "The area of the circle is: " << area << endl;
    return 0;
}
```

6) Number is odd or even

```cpp
#include <iostream>
using namespace std;

bool isEven(int num) {
    return (num % 2 == 0);
}

int main() {
    int number = 7;
    if (isEven(number)) {
        cout << number << " is even." << endl;
    } else {
        cout << number << " is odd." << endl;
    }
    return 0;
}
```

7) Factorial of number

```cpp
#include <iostream>
using namespace std;

int factorial(int n) {
    if (n == 0 || n == 1) {
        return 1;
    }
    return n * factorial(n - 1);
}

int main() {
    int n = 5;
    int fact = factorial(n);
    cout << "Factorial of " << n << " is: " << fact << endl;
    return 0;
}
```

8) Number is prime or not

```cpp
#include <iostream>
using namespace std;

bool isPrime(int num) {
    if (num <= 1) return false;
    if (num <= 3) return true;
    if (num % 2 == 0 || num % 3 == 0) return false;
    for (int i = 5; i * i <= num; i += 6) {
        if (num % i == 0 || num % (i + 2) == 0) return false;
    }
    return true;
}

int main() {
    int number = 23;
    if (isPrime(number)) {
        cout << number << " is prime." << endl;
    } else {
        cout << number << " is not prime." << endl;
    }
    return 0;
}
```

9) Print all prime numbers from 1 to n

```cpp
#include <iostream>
using namespace std;

bool isPrime(int num) {
    if (num <= 1) return false;
    if (num <= 3) return true;
    if (num % 2 == 0 || num % 3 == 0) return false;
    for (int i = 5; i * i <= num; i += 6) {
        if (num % i == 0 || num % (i + 2) == 0) return false;
    }
    return true;
}

void printPrimes(int n) {
    for (int i = 2; i <= n; ++i) {
        if (isPrime(i)) {
            cout << i << " ";
        }
    }
    cout << endl;
}

int main() {
    int n = 30;
    cout << "Prime numbers from 1 to " << n << " are: ";
    printPrimes(n);
    return 0;
}
```

10) Why can't we calculate factorial above 13?
- This is because the factorial of numbers grow very quickly and can exceed the maximum value that can be stored in a standard `int` data type.

11) Reverse an integer

```cpp
#include <iostream>
using namespace std;

int reverseInteger(int num) {
    int reversed = 0;
    while (num != 0) {
        reversed = reversed * 10 + num % 10;
        num /= 10;
    }
    return reversed;
}

int main() {
    int num = 12345;
    int reversedNum = reverseInteger(num);
    cout << "Reversed number: " << reversedNum << endl;
    return 0;
}
```

12) Set the ith bit

```cpp
#include <iostream>
using namespace std;

int setBit(int num, int i) {
    return num | (1 << i);
}

int main() {
    int num = 5; // Binary: 0101
    int i = 1;  // Set the 2nd bit (0-based index)
    int result = setBit(num, i); // Result: 7 (Binary: 0111)
    cout << "Result: " << result << endl;
    return 0;
}
```

13) Convert celsius to fahrenheit.

```cpp
#include <iostream>
using namespace std;

double celsiusToFahrenheit(double celsius) {
    return (celsius * 9/5) + 32;
}

int main() {
    double celsius = 25.0;
    double fahrenheit = celsiusToFahrenheit(celsius);
    cout << celsius << " degrees Celsius is equal to " << fahrenheit << " degrees Fahrenheit." << endl;
    return 0;
}
```
