## ISO 8583 Test Case :computer:


| No |   Test Type   |        Test Case Description       |     Step to Reproduce                     |   Expected Result   |   Result   |   Note (if any)   
|:--:|:-------------:|:----------------------------------:|:-----------------------------------------:|:-------------------:|:----------:|:-------------------:|
| 1  |    Positive   | Purchase Transaction Normal        | 1 Input amount <br> 2.Input valid password| Get RC 00           | PASSED     | None
| 2  |    Negative   | Purchase Insufficient Funds        | 1 Input amount more than saldo            | Get RC 51           | PASSED     | None
| 3  |    Negative   | Purchase Expired Card              | 1 Input amount <br> 2.Input valid password| Get RC 54           | PASSED     | None
| 4  |    Negative   | Purchase Incorrect PIN             | 1 Input amount <br> 2.Input inalid password| Get RC 55           | PASSED     | None

## UI Test Case :computer:

| No |   Test Type   |        Test Case Description       |     Step to Reproduce                                                                                                 |   Expected Result                         |   Result   |   Note (if any)   
|:--:|:-------------:|:----------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------:|:----------:|:-------------------:|
| 1  |    Positive   | Login success                      | 1 Open https://opensource-demo.orangehrmlive.com/ <br> 2.Input valid username and password <br>3. click "Login" Button| Login successful and dashboard page shown | PASSED     | None
| 2  |    Negative   | Login with invalid password        | 1 Open https://opensource-demo.orangehrmlive.com/ <br> 2.Input a valid username <br>3. Input an invalid password <br> 4. click "Login" Button| Login failed and error message "Invalid credentials" shown | PASSED     | None
| 3  |    Negative   | Login with invalid username        | 1 Open https://opensource-demo.orangehrmlive.com/ <br> 2.Input an invalid username <br>3. Input a valid password <br> 4. click "Login" Button| Login failed and error message "Invalid credentials" shown | PASSED     | None
| 4  |    Negative   | Login with empty fields            | 1 Open https://opensource-demo.orangehrmlive.com/ <br> 2.Leave username and password blank <br> 3. click "Login" Button| Error message "required" shown | PASSED     | None
| 5  |    Negative   | Login with only username filled    | 1 Open https://opensource-demo.orangehrmlive.com/ <br> 2.Input a valid username <br>3. Leave password empty <br> 4. click "Login" Button| Login failed and error message "required" shown | PASSED     | None
| 6  |    Negative   | Login with only upassword filled   | 1 Open https://opensource-demo.orangehrmlive.com/ <br> 2.Leave password empty <br>3. Input a valid password <br> 4. click "Login" Button| Login failed and error message "required" shown | PASSED     | None
