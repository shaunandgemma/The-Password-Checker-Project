Pwned Passwords Checker

This Python script checks if a password has been compromised in a data breach using the Pwned Passwords API. It works by taking the first 5 characters of the SHA-1 hash of a password and checking if it matches any of the hashes in the API's database. If a match is found, it means the password has been leaked and compromised.

Usage
To use this script, you need to pass one or more passwords as arguments when running the script. For example:

bash
Copy code
python3 check_password.py password123 mysecretpass 12345678
The script will check each password and print whether it has been found in any data breaches.

Dependencies
This script requires the requests module to make HTTP requests and the hashlib module to hash the passwords. You can install them using pip:

bash
Copy code
pip install requests hashlib
Limitations
Note that this script only checks against the Pwned Passwords database, which may not contain all compromised passwords. Also, it is not recommended to pass sensitive passwords as command-line arguments, as they can be visible in the process list. It's better to prompt the user for input or read passwords from a file.
