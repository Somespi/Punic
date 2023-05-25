# Punic

Punic is a lightweight and user-friendly unit testing framework for C++. It provides developers with an easy and efficient way to write and execute tests for their C++ code. Automated testing is crucial for ensuring code correctness, and C++Unit aims to simplify the process with its intuitive and flexible features.

## Features

- **Easy Integration:** Punic can be easily integrated into your C++ projects, allowing you to seamlessly incorporate unit tests into your development workflow.

- **Simple Assertion:** The framework provides an `assert` function that allows you to make assertions on the expected and actual values of your code. It supports various data types and automatically generates informative output.

- **Output Formatting:** The output of the test results is formatted in a clear and readable manner. Punic supports colored outputs, making it easier to distinguish between passed and failed tests. It also provides detailed information about assertion failures, including the expected and actual values.

- **Customizable:** Punic is designed to be flexible and customizable. You can extend its functionality according to your specific requirements. For example, you can add additional output formatting options or integrate it with other testing tools or frameworks.

## Getting Started

To start using Punic, simply clone the repository and integrate the framework into your C++ project.
Here's an example of how to write tests using Punic:

```cpp
#include "Punic.h"

bool isEven(int number) {
    return number % 2 == 0;
}

int main() {
    Punic p;

    // Test cases
    p.assert(true, []() { return isEven(2); }, "Even");
    p.assert(false,[]() { return isEven(7); }, "Odd");
    p.assert(true, []() { return isEven(0); }, "Zero");

    return 0;
}
```

When you run your test program, the test results will be displayed in the console output. Each test case will be listed with its corresponding name, status (PASSED or FAILED), and additional information if applicable (e.g., expected and actual values).

 

## Contributions

Contributions to Punic are welcome! If you find any issues or have suggestions for improvements, please open an issue in the repository. Additionally, feel free to submit pull requests for bug fixes, new features, or enhancements.

## License

Punic is released under the MIT License. See the LICENSE file for more details.
