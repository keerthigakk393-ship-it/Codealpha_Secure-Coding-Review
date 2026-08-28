TASK 3 – Secure Coding Review: 
1.	Select the Application
o	Programming Language: Python
o	Application: Login System
o	Platform: Kali Linux
2.	Create the Project Folder
        mkdir SecureCodingReview
                cd SecureCodingReview
3.	Create a Vulnerable Login Program
o	Create login1.py.
o	Use a simple login system with a hardcoded username and password.
4.	Run the Application
                       python3 login1.py
o	Test both valid and invalid login credentials.
o	Capture the output as evidence.
5.	Install the Static Analysis Tool
               sudo apt update
                       sudo apt install bandit -y
o	Verify the installation:
                                 bandit --version
6.	Perform Static Code Analysis
                        bandit login1.py
o	Analyze the security warnings reported by Bandit.
o	Record the identified vulnerabilities.
7.	Perform Manual Code Review
Check the code for:
o	Hardcoded credentials
o	Plain-text password storage
o	Improper input validation
o	SQL Injection
o	Weak authentication
o	Unlimited login attempts
o	Sensitive information exposure
8.	Identify Security Vulnerabilities
o	Example: Hardcoded Password – High Risk
o	Explain why each vulnerability is dangerous and what attack it could enable.
9.	Remediate the Vulnerabilities
o	Remove hardcoded credentials.
o	Use environment variables or secure secret storage.
o	Use password hashing.
o	Validate user input.
o	Use parameterized SQL queries.
o	Implement login attempt restrictions.
o	Use generic error messages.
10.	Create the Secure Version
o	Create secure_login.py.
o	Implement the recommended security practices.
11.	Test the Secure Application
                       python3 secure_login1.py
o	Test valid and invalid login attempts.
o	Verify that the application works correctly.
12.	Perform a Final Security Scan
                         bandit secure_login1.py
o	Compare the results with the original vulnerable code.
13.	Document the Findings
Prepare a table containing:
o	Vulnerability
o	Severity
o	Description
o	Risk
o	Recommended Fix
o	Remediation Status
14.	Final Result
o	The Python login application was successfully audited using manual code review and Bandit static analysis.
o	Security vulnerabilities were identified and remediated.
o	Secure coding practices were implemented to make the application safer and more resistant to common attacks.

