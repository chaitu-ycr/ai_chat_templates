# Python Package Review & Refactoring Template

---

## 🏁 Goal
Review the provided Python package and refactor it according to the user's specific request. Refactoring should improve code readability, performance, maintainability, and testability while preserving functionality.

## ✅ Example User Request
> "Please refactor the main module to use async functions and improve error handling using custom exceptions."

---

## 📚 Context
The package is designed to perform a specific set of tasks or provide certain functionality as described by the user. It may consist of multiple modules, subpackages, or utility files. The user may request changes such as:
- Refactoring synchronous code to async (see [Async Refactoring](#-async-refactoring))
- Improving logging and error handling (see [Custom Exceptions & Error Handling](#-custom-exceptions--error-handling))
- Removing deprecated functions and using modern Python features
- Enhancing performance, readability, maintainability, or testability
- Adopting best practices for Python packaging and distribution

---

## 📝 Review Workflow Checklist
- [ ] Clarify the user request and goals
- [ ] Analyze the codebase for improvements (structure, style, dependencies)
- [ ] Refactor code incrementally, following best practices
- [ ] Add inline comments explaining rationale for changes
- [ ] Ensure all unit tests pass or update/add tests as needed
- [ ] Document changes and summarize key improvements/issues
- [ ] Update documentation (README, docstrings, API docs) if public interfaces change
- [ ] Review and update semantic versioning if public APIs are modified
- [ ] Check for security issues and validate input handling
- [ ] Ensure consistent use of type hints and docstrings

---

## ⚡ Async Refactoring
- Use `async def` and `await` for I/O-bound operations
- Replace blocking calls (e.g., `requests`) with async alternatives (e.g., `aiohttp`)
- Ensure event loop management is correct
- Avoid mixing sync and async code to prevent deadlocks or performance issues

---

## 🚨 Custom Exceptions & Error Handling
- Define custom exception classes for domain-specific errors
- Use `try`/`except` blocks to handle expected errors gracefully
- Log errors using the `logging` module
- Avoid catching broad exceptions (e.g., `except Exception:`) unless necessary
- Provide informative error messages and propagate exceptions appropriately

```python
class MyCustomError(Exception):
    """Custom exception for specific error cases."""
    pass

try:
    # ... code ...
except MyCustomError as e:
    logging.error(f"Error occurred: {e}")
```

---

## ⚠️ Common Pitfalls
- Missing or outdated type hints and docstrings
- Not running or updating tests after refactoring
- Overlooking deprecated, unused, or duplicate code
- Inconsistent formatting, naming conventions, or import order
- Hardcoded values or magic numbers; prefer constants or configuration
- Lack of input validation or insufficient error handling

---

## 🛠️ Code Quality Tools
- [`black`](https://black.readthedocs.io/) for code formatting
- [`ruff`](https://docs.astral.sh/ruff/) or [`flake8`](https://flake8.pycqa.org/) for linting
- [`mypy`](http://mypy-lang.org/) for type checking
- [`pre-commit`](https://pre-commit.com/) hooks to automate code quality checks
- [`pytest`](https://docs.pytest.org/) for testing and coverage
- [`bandit`](https://bandit.readthedocs.io/) for security linting

---

## 📂 Source
The source code may be organized across one or more modules, subpackages, or utility files. Assume Python 3.10+ standards and common libraries such as `requests`, `asyncio`, and `logging`.
- Prefer modular design and separation of concerns
- Remove unused imports and dependencies
- Ensure all public APIs are documented

---

## 🧾 Expectations
- Provide inline code suggestions or refactored snippets with comments explaining rationale
- Highlight potential issues or improvements
- Maintain consistent formatting and naming conventions
- Ensure compatibility with existing unit tests (if present)
- Add or update type hints and docstrings where missing
- Run code quality tools and address any issues
- Update documentation and versioning if APIs change
- Ensure code is secure, testable, and maintainable

---

## 🧪 Test Compatibility
- Run all unit tests after refactoring; update or add tests if new functionality or exceptions are introduced
- Check test coverage and add tests for uncovered code paths

---

## 📖 Documentation Updates
- Update README, usage examples, and API documentation if public interfaces or behaviors change
- Ensure docstrings are accurate, complete, and follow standards (e.g., Google style)
