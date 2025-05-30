# 🔒 Password Authentication System with PostgreSQL and Python

<p align="center">
  <img src="https://github.com/user-attachments/assets/19808360-d11e-4faf-81e3-ae847ac6912b" alt="System Architecture" width="1080"/>
</p>

A secure user authentication system using PostgreSQL and Python, featuring bcrypt password hashing and strong password validation. Includes Gradio UI and runs in Google Colab.
Live Link to the app (Hosted on Huggingface): [App](https://huggingface.co/spaces/abdulrafaymohammed/userpasswordauthapp)
## ✨ Features

- ✅ **Zero Trust Design**: 8-point password validation
- 🔐 **Military-Grade Security**: BCrypt + salt hashing
- 🗄️ **Cloud-Native**: PostgreSQL via Neon.tech
- 🧪 **Colab-Ready**: Jupyter notebook included
- 🖥️ **User-Friendly**: Gradio web interface

```mermaid
graph TD
    A[Gradio UI] -->|User Input| B[Python Auth System]
    B -->|Hash/Verify| C[PostgreSQL Database]
    C -->|Cloud Storage| D[Neon.tech Hosting]
    B -->|Security Checks| E[Password Validator]
    E -->|8 Rules| F[(Secure Storage)]
```
## Preview of what was achieved
- Neon Postgre Database:
   <p align="center">
  <img width="800" alt="Neon PostgreSQL Database" src="https://github.com/user-attachments/assets/be90130e-3cc5-48d1-bbc3-a0491918053e" />
</p>


- Signup Page:
<p align="center">
<img width="1512" alt="Screenshot 2025-05-30 at 12 34 24 PM" src="https://github.com/user-attachments/assets/34479e7a-dac6-46c1-853e-3d95600185f9" />
</p>

- Login Page:
<p align="center">
<img width="1498" alt="Screenshot 2025-05-30 at 12 43 32 PM" src="https://github.com/user-attachments/assets/64665796-1a58-45b4-a5f2-b2964c989119" />
</p>

## 🛠️ Prerequisites
### Database Setup
- Create a PostgreSQL database on Neon.tech
- Select your preferred region (Azure East-US recommended)
- Retrieve your connection string from Neon Console > Connect to your database
- Example:
  ``` html
  postgresql://neondb_owner:your_password@ep-your-instance.eastus2.azure.neon.tech/neondb?sslmode=require
  ```
### Google Colab Setup
- Create a Google account for Colab access
- Open the provided Google Colab notebook

## ⚡ Quick Start
- Install dependencies:
``` python
!pip install bcrypt psycopg2-binary gradio
```
- Configure your database credentials in the notebook
- Run the setup cells in auth.py to create the users table
- Test authentication with:
  - signup() - Create new users
  - login() - Authenticate existing users
- Launch the Gradio UI in app.py
``` mermaid
pie title Password Requirements
    "Length ≥8" : 15
    "Upper+Lower Case" : 15
    "Digits" : 15
    "Special Chars" : 15
    "No Spaces" : 10
    "No Common Passwords" : 20
    "Max 2 Repeats" : 10
```
### Passwords must:

- Be at least 8 characters  
- Include uppercase and lowercase letters  
- Contain digits and special characters
``` python
  # Common passwords list
COMMON_PASSWORDS = {"123456", "password", "12345678", "qwerty", "abc123"}
``` 
- Have no spaces  
- Avoid common passwords  
- Not have more than 2 repeated characters in a row  

## License

This project is open source under the [MIT License](LICENSE).
