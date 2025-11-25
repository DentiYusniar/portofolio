# Sample Bug Report
## Overview

In this repository, we follow best practices for bug reporting to ensure effective communication and resolution of issues. Our approach includes:

1. **Detailed Descriptions:** Clearly describing the bug, steps to reproduce, and expected vs. actual behavior.
2. **Reproducibility:** Providing a detailed set of steps to reproduce the issue to help developers quickly identify and address the problem.
3. **Context:** Including environment details and any additional context that might help in diagnosing the issue.
4. **Severity Classification:** Categorizing the bug based on its impact to prioritize the fix.
5. **Testing:** Suggesting test cases to verify that the bug has been fixed.

By adhering to these practices, we aim to streamline the bug resolution process and enhance the quality of our software.

---

## Summary
**Brief description of the bug:** When logging in with a non-case-sensitive password, the user is able to log in successfully.

---

## Steps to Reproduce
1. Open the login page
2. Input username and insensitive password
3. Click "Login" button

---

## Expected Result
The system should prevent the user from logging in when entering a password with incorrect letter casing. The login attempt should fail and an error message should be displayed.

---

## Actual Result
The user is able to log in succesfuully even when entering the password with incorrect letter casing.

---

## Evidaence
**If applicable, add screenshots to help explain your problem:**
<img width="1364" height="650" alt="image" src="https://github.com/user-attachments/assets/9ad351d0-1eb4-4122-ba6b-6a6d23c78502" />


---

## Environment
- **[X] QA**
- **[ ] Staging**
- **[ ] Production**

---

## Additional Context
**Add any other context about the problem here, such as logs, configuration files, or related issues:**

- Error log snippet:

---

## Possible Solution
**If you have an idea of how to fix the bug, please describe it here:**

- Ensure that the password validation process treats passwords as case-sensitive.
- Update the authentication logic so that both the frontend and backend compare the entered password exactly as stored in the database, including uppercase and lowercase characters.
- Additionally, review the hashing and verification methods to confirm they do not unintentionally normalize or alter character cases.

---

## Severity
- **[X] Critical** - Blocks all work, requires immediate fix
- **[ ] Major** - Significant impact but not a showstopper
- **[ ] Minor** - Low impact, cosmetic issues
---
