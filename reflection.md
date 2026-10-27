# Lab 5 — Static Code Analysis Reflection

### 1. What is static code analysis?

Static code analysis examines source code without executing it to identify potential bugs, security vulnerabilities, and coding-standard violations. It improves code quality, security, and maintainability.

### 2. What are the differences between Pylint, Bandit, and Flake8?

- **Pylint:** Identifies code-quality issues, naming problems, unused variables, and missing documentation.
- **Bandit:** Detects potentially insecure Python coding patterns.
- **Flake8:** Checks Python style and formatting, including line length, unused imports, and whitespace.

### 3. What issues were identified and fixed?

The analysis identified unsafe use of `eval()`, weak MD5 hashing, shell-command execution, broad exception handling, insecure random-number generation, a mutable default argument, unused variables, and formatting problems. The code was updated to address these issues.

### 4. What were the results after fixing the issues?

The final Pylint score was 10.00/10, compared with 5.19/10 initially. Bandit reported no issues, and Flake8 produced no reported violations.

### 5. What did you learn from this lab?

I learned how to use Pylint, Bandit, and Flake8 to improve Python code quality and security. I also learned that static analysis should be combined with program execution and functional testing to verify that code changes preserve the intended behaviour.
