# Password Authentication System with PostgreSQL and Python

<p align="center">
  <img src="https://github.com/user-attachments/assets/19808360-d11e-4faf-81e3-ae847ac6912b" alt="totp-10" width="1020"/>
</p>

A simple, secure user authentication system using PostgreSQL and Python (Google Colab). Features bcrypt password hashing and enforces 8 strong password rules to ensure safe signup and login.

---

## Features

- ✅ User signup with password strength validation  
- 🔐 Secure password storage using bcrypt hashing  
- 🔓 User login with password verification  
- 🗄️ PostgreSQL database backend (cloud-hosted)  
- 🧪 Easy to run on Google Colab  

---

## Getting Started

### Prerequisites

- PostgreSQL database (I am using PG Admin to access Postgre Databases)  
- Google account to use Google Colab  

### Setup

1. Clone this repo or open the provided Google Colab notebook.  
2. Install dependencies in Colab:
   ```python
   !pip install bcrypt psycopg2-binary
   ```
3. Enter your PostgreSQL credentials in the notebook.  
4. Run the setup cells to create the `users` table.  
5. Use the `signup()` and `login()` functions to test authentication.  

---

## Password Rules

Passwords must:

1. Be at least 8 characters  
2. Include uppercase and lowercase letters  
3. Contain digits and special characters  
4. Have no spaces  
5. Avoid common passwords  
6. Not have more than 2 repeated characters in a row  

---

## License

This project is open source under the [MIT License](LICENSE).
