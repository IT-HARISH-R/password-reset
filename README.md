# Authentication and Password Reset API

This project is a Node.js-based backend application providing authentication functionalities like user registration, login, password reset via email, and token-based authentication.

## Features
- **User Registration:** Create a new account with an email, username, and password.
- **Login:** Authenticate users with email and password, issuing a JWT token.
- **Forgot Password:** Send a password reset link to the user's registered email.
- **Reset Password:** Update the user's password using the token sent in the email.
- **Token-Based Authentication:** Secure endpoints with JSON Web Tokens (JWT).

## Technologies Used
- **Node.js**: Server-side runtime.
- **Express.js**: Web framework for Node.js.
- **MongoDB**: NoSQL database to store user details.
- **Mongoose**: MongoDB object modeling for Node.js.
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
  "email": "example@example.com",
  "password": "examplePassword"
}
```
* Response: Success or error message.

2. Login

* Endpoint: ```/auth/login```
* Method: ```POST```

```bash
{
  "email": "example@example.com",
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
  "email": "example@example.com"
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
│   └── userModels.js      # User schema definition
├── controllers/
│   └── userController.js  # User-related logic
├── routers/
│   └── authRout.js        # Authentication routes
├── utils/
│   ├── config.js          # Configuration (e.g., secrets)
│   ├── logger.js          # Logging middleware
│   └── errorPage.js       # Error handling middleware
├── app.js                 # Main application file
├── README.md              # Project documentation
├── package.json           # Dependencies and scripts
└── .env                   # Environment variables
```