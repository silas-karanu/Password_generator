# Password_generator
Importing modules from the Python standard library and using Regular Expressions by building a password generator program.

# 🔐 Secure Password Generator in Python

This project provides a secure and customizable password generator written in Python. It uses cryptographically secure random generation (`secrets`) and allows you to enforce specific character requirements such as digits, special characters, uppercase and lowercase letters.

---

## 📦 Features

- ✅ Secure random generation using `secrets.choice()`
- 🔢 Enforce minimum counts for:
  - Digits
  - Special characters
  - Uppercase letters
  - Lowercase letters
- ⚙️ Fully customizable password length and character constraints
- 🔄 Automatically retries until a valid password is generated

---

## 🚀 Usage

### ➤ Run the Script

```bash
python password_generator.py
```
---

## 🧠 How It Works
1. The scripts defines a character pool from:
    - ASCII letters (uppercase and lowercase)

    - Digits (0–9)

    - Punctuation (special characters)
2. It repeatedly generates a password until all specified constraints are met using regular expressions (`re.findall()`).
3. Passwords are generated with `secrets.choice()` to ensure they are secure for cryptographic purposes.

---

## ✏️ Customization
You can customize password generation by modifying the function parameters:
```python
generate_password(length=20, nums=2, special_chars=2, uppercase=3, lowercase=2)
```

| Parameter       | Description                          | Default |
| --------------- | ------------------------------------ | ------- |
| `length`        | Total length of the password         | 16      |
| `nums`          | Minimum number of digits             | 1       |
| `special_chars` | Minimum number of special characters | 1       |
| `uppercase`     | Minimum number of uppercase letters  | 1       |
| `lowercase`     | Minimum number of lowercase letters  | 1       |

---

## 📂 File Structure
```text
password_generator.py    # Main script
README.md                # Project documentation
```

---

## 🛡️ Requirements
- Python 3.6 or later (uses secrets module)

---

## 📃 License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 🚧 Future Improvements

When you revisit this project, consider adding or improving the following:

- Constraint-aware password construction
 Build the required characters first, then fill the rest randomly and shuffle — improves efficiency vs. retry-based generation.

- Unit testing
 Add tests to verify that constraints are enforced and edge cases are handled properly.

- Command-line interface (CLI)
 Use argparse to allow users to specify options via terminal flags.

- GUI or web version
 Add a simple user interface using Flask (web) or Tkinter/PyQt (desktop).

- Password strength indicator
 Estimate password strength using entropy or a scoring system.

- Pattern avoidance
 Improve randomness logic to avoid repeated or predictable character sequences.

- Verbose/debug mode
 Optionally log how many attempts were needed and what constraints failed.

---

## 📌 Notes
- Passwords are randomly shuffled and validated for constraints.

- Ensure that the sum of constraint values does not exceed the total password length.

---