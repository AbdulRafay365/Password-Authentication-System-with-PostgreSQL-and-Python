# 🔒 Password Authentication System with PostgreSQL and Python

<p align="center">
  <img src="https://github.com/user-attachments/assets/19808360-d11e-4faf-81e3-ae847ac6912b" alt="System Architecture" width="720"/>
</p>

A secure authentication system combining Python's bcrypt hashing with PostgreSQL for cloud-ready user management. Features Gradio UI and runs seamlessly in Google Colab.

## 🌟 Features

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
## 🚀 Getting Started
Prerequisites
PostgreSQL database (PGAdmin recommended)

Google account for Colab access

⚡ Quick Setup
``` python
!pip install bcrypt psycopg2-binary gradio
```

Import the Colab notebook

Configure your Neon.tech credentials

Run all cells to activate the Gradio UI
```mermaid 
pie title Password Requirements
    "Length ≥8" : 15
    "Upper+Lower Case" : 15
    "Digits" : 15
    "Special Chars" : 15
    "No Spaces" : 10
    "No Common Passwords" : 20
    "Max 2 Repeats" : 10
```
