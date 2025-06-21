# MinUnit_Min: A Lightweight Unit Testing Framework for C 🚀

![MinUnit](https://img.shields.io/badge/MinUnit-Minimal%20Setup-brightgreen)

Welcome to the **MinUnit_Min** repository! This project provides a minimal setup for **MinUnit**, a lightweight unit testing framework designed specifically for C programming. Whether you are developing embedded systems or just want to ensure your C code is reliable, this framework offers a straightforward way to implement unit tests without any external dependencies.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Getting Started](#getting-started)
- [Example Usage](#example-usage)
- [Test Automation](#test-automation)
- [Contributing](#contributing)
- [License](#license)
- [Releases](#releases)

## Introduction

MinUnit is a header-only testing framework that allows developers to add unit tests to their C projects quickly. It focuses on simplicity and efficiency, making it an excellent choice for both beginners and experienced developers. The lightweight nature of MinUnit means that it won't bloat your project or slow down your development process.

## Features

- **Header-Only**: Just include `minunit.h` in your project.
- **No Dependencies**: MinUnit requires no external libraries or frameworks.
- **Easy Integration**: Quickly add unit tests to any C project.
- **Test Automation**: Basic scripts are included to automate the testing process.
- **Example Tests**: Learn by example with included test cases.

## Getting Started

To get started with MinUnit, follow these steps:

1. **Clone the Repository**:
   Open your terminal and run the following command:
   ```bash
   git clone https://github.com/Smoke667/minunit_min.git
   ```

2. **Include MinUnit**:
   Add `minunit.h` to your C project. You can find it in the cloned repository.

3. **Write Your Tests**:
   Create a new C file for your tests. Use the examples provided to structure your tests.

4. **Compile and Run**:
   Compile your tests with your C compiler and run the resulting executable.

## Example Usage

Here’s a simple example to demonstrate how to use MinUnit.

### Sample Test Case

```c
#include "minunit.h"

MU_TEST(test_addition) {
    mu_check(1 + 1 == 2);
}

MU_TEST(test_subtraction) {
    mu_check(2 - 1 == 1);
}

MU_TEST_SUITE(test_suite) {
    MU_RUN_TEST(test_addition);
    MU_RUN_TEST(test_subtraction);
}

int main(int argc, char *argv[]) {
    MU_RUN_SUITE(test_suite);
    MU_REPORT();
    return 0;
}
```

### Explanation

- **MU_TEST**: Defines a test case.
- **mu_check**: Asserts that the condition is true.
- **MU_RUN_TEST**: Runs the specified test case.
- **MU_RUN_SUITE**: Runs all tests in the suite.
- **MU_REPORT**: Prints the results of the tests.

## Test Automation

To facilitate test automation, the repository includes basic scripts that you can use. These scripts will help you run your tests quickly and efficiently. You can find them in the `scripts` directory.

### Running Tests Automatically

You can execute the following command to run your tests automatically:

```bash
./scripts/run_tests.sh
```

This script will compile your test files and run them, providing you with a report of the results.

## Contributing

We welcome contributions to MinUnit_Min! If you have suggestions, improvements, or bug fixes, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes.
4. Commit your changes with a clear message.
5. Push your branch to your fork.
6. Create a pull request.

Your contributions help improve this framework for everyone.

## License

MinUnit_Min is licensed under the MIT License. Feel free to use it in your projects, but please give credit where it's due.

## Releases

To download the latest version of MinUnit, visit the [Releases section](https://github.com/Smoke667/minunit_min/releases). You can find all the necessary files there, including the latest updates and improvements.

If you encounter any issues or need older versions, please check the **Releases** section on GitHub.

## Conclusion

MinUnit_Min is a powerful yet simple tool for unit testing in C. Its minimal setup and ease of use make it a great choice for developers who want to ensure their code is reliable without the overhead of complex frameworks. 

For more information, examples, and updates, feel free to visit the [Releases section](https://github.com/Smoke667/minunit_min/releases). Happy coding!