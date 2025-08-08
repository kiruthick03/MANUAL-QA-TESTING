# Login Application Test Cases

> App: Sample Login Application  
> Environment: Windows 10 / Chrome latest, Firefox latest

| Test Case ID | Title | Precondition | Test Steps | Test Data | Expected Result | Actual Result | Severity | Priority | Status |
|--------------|-------|--------------|------------|-----------|-----------------|---------------|----------|----------|--------|
| TC001 | Valid login | App reachable, valid user exists | 1. Open browser <br> 2. Go to /login <br> 3. Enter username & password <br> 4. Click **Login** | username: user1 <br> password: Pass@123 | User is logged in and redirected to dashboard | As Expected | High | P1 | Pass |
| TC002 | Invalid password | App reachable | Enter valid username but wrong password | username: user1 <br> password: WrongPass | Error: "Invalid credentials" | As Expected | Medium | P2 | Pass |
| TC003 | Blank username | App reachable | Leave username blank, enter valid password | username: "" <br> password: Pass@123 | Error: "Username required" | As Expected | Low | P3 | Pass |
| TC004 | Blank password | App reachable | Enter username, leave password blank | username: user1 <br> password: "" | Error: "Password required" | As Expected | Low | P3 | Pass |
| TC005 | SQL injection attempt | App reachable | Enter `' OR 1=1 --` in username field | `' OR 1=1 --` | Login must fail; input sanitized | As Expected | High | P1 | Pass |
