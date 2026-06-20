# Python Calculator Project

[![Run Python Tests](https://github.com/Kennyjaymes/Python-Calculator-Project/actions/workflows/python-tests.yml/badge.svg)](https://github.com/Kennyjaymes/Python-Calculator-Project/actions/workflows/python-tests.yml)

A simple, robust Python calculator application equipped with unit tests and automated CI/CD workflow via GitHub Actions.

## Features

- **Addition**: Sums two numbers.
- **Subtraction**: Calculates the difference between two numbers.
- **Multiplication**: Multiplies two numbers.
- **Division**: Divides one number by another (with safe division-by-zero handling raising a `ValueError`).

## Project Structure

```text
├── .github/
│   └── workflows/
│       └── python-tests.yml   # GitHub Actions CI workflow
├── .gitignore                  # Python Git ignore file
├── calculator.py               # Calculator core implementation
├── test_calculator.py          # Unit tests
└── README.md                   # Project documentation
```

## Getting Started

### Prerequisites

- Python 3.x

### Running the App

The calculator logic is exposed via `calculator.py`. You can import the functions directly into your Python scripts:

```python
import calculator

print(calculator.add(10, 5))       # Output: 15.0
print(calculator.divide(10, 2))    # Output: 5.0
```

### Running Tests Locally

You can run the test suite locally using Python's built-in `unittest` module:

```bash
python -m unittest discover -s . -p "test_*.py"
```

*Note: Depending on your system configuration, you might need to use `python3` or a specific version executable like `python3.14`.*

## Continuous Integration (CI)

This project is configured with a GitHub Actions workflow that automatically runs all unit tests on:
- Every push to any branch.
- Every pull request.

The workflow configuration is defined in `.github/workflows/python-tests.yml`.
