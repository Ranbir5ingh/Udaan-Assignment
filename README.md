# MERN Stack User Authentication System

## Description
This project is a User Authentication System built using the MERN stack (MongoDB, Express.js, React.js, Node.js). It implements a JWT-based authentication system that allows users to register, log in, and access protected routes. The system includes features such as password hashing, error handling, and input validation.

## Assignment Overview
### MERN Stack Intern Assignment
**Task**: Build a User Authentication System (Backend Focused)

**Requirements**:
- **User registeration**: Implemented with email & password validation.
- **User login**: JWT token generation upon successful login.
- **Protected routes**: Only logged-in users can access certain endpoints.
- **Backend**: Built using Express.js + MongoDB.
- **Password hashing**: Implemented using bcrypt.js.
- **Error handling & input validation**: Proper error handling and input validation are included.

### Bonus Points:
- **Role-Based Access Control (RBAC)**: Users can have different roles (Admin & User).
- **Deployment**: The application is deployed on Vercel.

## User Access Levels
- Users will have access to the user view only.
- Admins will have a different admin view that cannot be accessed by users.
- Admins cannot access the user view.

### Testing Credentials
For testing purposes, you can use the following credentials to log in as an admin in the Vercel live deployment:
- Email: `admin@gmail.com`
- Password: `admin123`


## Technologies Used
- **Backend**: 
  - Node.js
  - Express.js
  - MongoDB
  - bcrypt.js (for password hashing)
  - jsonwebtoken (for JWT token generation)
- **Frontend**: 
  - React.js
  - Vite

## Installation Instructions
1. **Clone the repository**:
   ```bash
   git clone https://github.com/Ranbir5ingh/Udaan-Assignment.git
   cd Udaan-Assignment
   ```

2. **Navigate to the server directory and install dependencies**:
   ```bash
   cd server
   npm install
   ```

3. **Set up environment variables**:
   - Create a `.env` file in the `server/` directory and add the following:
     ```
     MONGO_URL=<MongoDB connection string with username and password>
     PORT=<Port number for the server (default is 5000)>
     CLIENT_BASE_URL=<Base URL for the client application>
     JWT_SECRET_KEY=<Secret key for JWT token generation>

     ```

   - Create a `.env` file in the `client/` directory and add the following:
     ```
     VITE_API_URL=<Base URL for the backend API>

     ```

4. **Navigate to the client directory and install dependencies**:
   ```bash
   cd ../client
   npm install
   ```

## Usage
1. **Start the backend server**:
   ```bash
   cd server
   node server.js
   ```

2. **Start the frontend application**:
   ```bash
   cd ../client
   npm run dev
   ```

3. **Access the application in your browser** at Client Base Url.

## API Endpoints
- **POST /api/auth/register**: User registration with email and password.
- **POST /api/auth/login**: User login with email and password.
- **POST /api/auth/logout**: User logout.
- **GET /api/auth/check-auth**: Check if the user is authenticated.

## User Roles
- The default role for new users is set to **user**. Users can have different roles (Admin & User).
- To change a user's role to **admin**, you must manually edit the user's role in the MongoDB database.

## Deployment
- The application is deployed on Vercel using a free plan. This may result in slower response times or timeout errors when connecting to the backend. If you encounter such issues, please be patient, try reloading the page, and ensure you have a good internet connection. There are no such issues when running the code on your local machine. You can access the deployment at the following URL: [Vercel Deployment Link](https://udaan-assignment.ranbirsingh.xyz/).
