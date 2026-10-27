# Lab 5 — Static Code Analysis: Issues and Fixes

| No. | Issue | Type | Line(s) | Description | Fix Approach |
|---:|---|---|---|---|---|
| 1 | Unsafe `eval()` | Security | 40 | May execute arbitrary Python expressions. | Replace with a safe, explicitly defined cost calculation. |
| 2 | Weak MD5 hash | Security | 45 | MD5 is unsuitable for security-sensitive hashing. | Use an appropriate secure hashing method or remove it if unnecessary. |
| 3 | Shell command execution | Security | 56 | `os.system()` executes a shell command. | Replace with normal Python output, such as `print()`. |
| 4 | Broad exception with `pass` | Bug/Security | 21–25 | Hides errors during patient discharge. | Catch the expected exception and handle it explicitly. |
| 5 | Insecure random token | Security | 49 | `random.randint()` is not designed for security tokens. | Use `secrets` if the ward token is security-sensitive. |
| 6 | Mutable default argument | Bug | 13 | A default list may be shared across function calls. | Use `None` and initialize a new list inside the function. |
| 7 | Unused imports and variables | Code quality | 4, 29, 39 | Unused `math`, `bed_charge`, and `base_bill`. | Remove them if they are unnecessary, or use them correctly. |
| 8 | Missing docstrings | Code quality | Multiple | Functions and the module lack documentation. | Add appropriate docstrings. |
| 9 | Long lines and formatting | Style | Multiple | Several lines exceed 79 characters. | Split long lines and follow PEP 8. |
| 10 | File handling and encoding | Code quality | 53 | File is opened without an explicit encoding and may not close safely after an error. | Use a `with open(..., encoding="utf-8")` block. |

