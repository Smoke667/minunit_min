# MinUnit Angellop

## Table of Contents
- [Project Description](#project-description)
- [Background](#background)
- [How to Compile and Run the Tests](#how-to-compile-and-run-the-tests)
- [How to Integrate MinUnit in Your Project](#how-to-integrate-minunit-in-your-project)
- [Common Errors and Solutions](#common-errors-and-solutions)
- [Related LinkedIn Post](#related-linkedin-post)
- [Connect](#connect)
  - [Who am I?](#who-am-i)
- [Keywords](#keywords)

## Project Description
This repository provides a minimal and easy-to-use MinUnit setup for unit testing in C. It includes the MinUnit header and a sample test, making it easy to add tests to any C project.

## Background
The motivation for this repository is to offer a quick and reusable base for anyone who wants to add unit tests to their C projects without external dependencies or complex configurations.

## How to Compile and Run the Tests

1. Compile the sample test:

```bash
cc -Iincludes test/test_dummy.c -o test_dummy
```

2. Run the test:

```bash
./test_dummy
```

## How to Integrate MinUnit in Your Project

1. Copy `minunit.h` to your project's include folder.
2. Write your tests in `.c` files using the MinUnit syntax:

```c
#include "minunit.h"

int tests_run = 0;

MU_TEST(test_example) {
    mu_assert("1 == 1", 1 == 1);
    return 0;
}

MU_TEST_SUITE(suite) {
    MU_RUN_TEST(test_example);
}

int main() {
    MU_RUN_SUITE(suite);
    MU_REPORT();
    return 0;
}
```

3. Add a rule to your Makefile to compile the tests. Example:

```makefile
test: test/test_example.c includes/minunit.h
	cc -Iincludes test/test_example.c -o test_example
	./test_example
```

You can create as many test files as you need and add similar rules to your Makefile.

---

MinUnit is simple, requires no installation or external dependencies. Just include the header and compile your tests.

## Common Errors and Solutions

### Error: minunit.h not found

**Symptom:**
The compiler cannot find the `minunit.h` file.

**Solution:**
Make sure to use the `-Iincludes` option (or the correct path) when compiling:

```bash
cc -Iincludes test/test_dummy.c -o test_dummy
```

### Error: tests_run not defined

**Symptom:**
Linker error for undefined symbol `tests_run`.

**Solution:**
Declare the global variable in each test file:

```c
int tests_run = 0;
```

## Related LinkedIn Post

🔗 **Learn more about projects and resources on my LinkedIn:**  
[Angello López Molina on LinkedIn](https://www.linkedin.com/in/angellopezmolina/)

## Connect

👉 **[Connect with me on LinkedIn!](https://www.linkedin.com/in/angellopezmolina/)** 👈

### Who am I?

I am a software developer based in Málaga, with experience in multiple languages and technologies. I am passionate about creating robust and efficient solutions, with a self-taught and scientific mindset. You can learn more about my professional background and projects on my [LinkedIn](https://www.linkedin.com/in/angellopezmolina/).

## Keywords
minunit, c, testing, unit test, example, integration, makefile, minimal, portable, simple, header-only, tdd, automated testing, open source
