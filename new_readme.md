# 🔒 Password Authentication System with PostgreSQL and Python

<p align="center">
  <img src="https://github.com/user-attachments/assets/19808360-d11e-4faf-81e3-ae847ac6912b" alt="System Architecture" width="1080"/>
</p>

A simple, secure user authentication system using PostgreSQL on the cloud and Python (Google Colab). Features bcrypt password hashing and enforces 8 strong password rules to ensure safe signup and login. Features Gradio UI and runs seamlessly in Google Colab.

## Features

- ✅ **Zero Trust Design**: 8-point password validation
- 🔐 **Military-Grade Security**: BCrypt + salt hashing
- 🗄️ **Cloud-Native**: PostgreSQL via Neon.tech (Azure East-US Region)
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
## Prerequisites
⚙️ Setting up the environment:
- On-the-cloud PostgreSQL database setup using Neon.tech (I am using Azure East-US Region) [Neon Link](https://neon.com/?gad_source=1&gad_campaignid=21329093217&gbraid=0AAAAAqiR81rI9vgsbrrFgzZ0_fVQ5Yf5w&gclid=CjwKCAjwruXBBhArEiwACBRtHTOM1yZN8eTiJDgyGEgkZThBMSz_zjnR8TpE6A7h75rJJqsnIZhX2hoCltQQAvD_BwE)
- Create a new Postgre Database. Select between Azure and AWS regions. I went with Azure East-US Region.
- Retrive a connection string on: Neon Console > Connect to your database > Replace with yours:
  ``` html
  postgresql://neondb_owner:*********@ep-hidden-salad-a8mx9yqn-pooler.eastus2.azure.neon.tech/neondb?sslmode=require (Where ****** will be your password.)
  
  ```
- Create a Google account for Colab access
- Clone this repo or open the provided Google Colab notebook.
  
⚡ Quick Notebook Setup:
- Install dependencies in Colab:
``` python
!pip install bcrypt psycopg2-binary gradio
```
- Enter your Neon.tech PostgreSQL credentials in the notebook.
- Run the setup cells to create the users table.
- Use the signup() and login() functions to test authentication.
- Run the Gradio UI cell for the UI.

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
## License

This project is open source under the [MIT License](LICENSE).
