Your prompt is well-structured and effectively communicates the requirements for setting up a comprehensive backend project. However, I noticed a few areas where it could be clarified or enhanced for better precision. Here's the revised prompt with additional details for clarity:

---

**Revised Prompt:**

"I need a complete backend project template for a Node.js and Express-based application with the following features:  

1. **Project Structure**: Follow a modular folder structure with directories for configuration, controllers, middlewares, models, routes, utilities, logs, and public assets. Specifically:  
```
backend-template/
├── src/
│   ├── config/
│   │   ├── db.js              # Database connection with retry logic and pool size options
│   │   └── env.js             # Loads environment variables using dotenv
│   ├── controllers/
│   │   ├── authController.js  # Handles authentication-related operations
│   │   ├── userController.js  # Handles user-related operations
│   └── middlewares/
│       ├── authMiddleware.js  # Verifies JWT and attaches user info to requests
│       ├── roleMiddleware.js  # Restricts access based on user roles
│       ├── errorHandler.js    # Centralized error handling middleware
│       ├── fileUpload.js      # Configures and validates file uploads
│   ├── models/
│   │   ├── User.js            # Mongoose schema for user management
│   ├── routes/
│   │   ├── authRoutes.js      # Routes for register, login, and password reset
│   │   ├── userRoutes.js      # Routes for user operations
│   ├── utils/
│       ├── email.js           # Utility for sending emails using nodemailer
│       ├── logger.js          # Logger implementation using fs and path
│       ├── pagination.js      # Utility for paginating API responses
│       ├── validators.js      # Centralized input validation logic
│   ├── app.js                 # Main Express app setup and route mounting
│   └── server.js              # Starts the server and listens for requests
├── logs/
│   ├── error.log              # Logs error messages
│   ├── combined.log           # Logs all application events
├── public/
│   └── uploads/               # Directory for uploaded files
├── .env                       # Environment variable configurations
├── .gitignore                 # Ignore sensitive files like node_modules and .env
├── README.md                  # Project setup and usage instructions
├── package.json               # Dependencies and scripts
├── postman-collection.json    # API testing collection for Postman
```

2. **Database**: Use MongoDB with Mongoose. Include a robust connection setup in `db.js` with:  
   - Connection pool size  
   - Retry logic for handling initial connection failures  
   - Proper error logging on connection failures.  

3. **Authentication & Authorization**:  
   - JWT-based authentication with token expiration (e.g., 1 hour).  
   - Role-based access control with middleware (`user`, `admin`).  
   - Include endpoints for:  
     - Register (with password hashing and email verification)  
     - Login (with validation and token generation)  
     - Password reset (with email notification).  

4. **File Upload**: Implement a file upload middleware using `multer`:  
   - Store uploaded files in `public/uploads/`.  
   - Restrict file types to images only (e.g., JPG, PNG).  

5. **Utilities**: Include:  
   - **Email utility**: Use `nodemailer` to send emails (e.g., password reset or welcome emails).  
   - **Logger utility**: Write logs (errors, events) to files in the `logs/` directory.  
   - **Pagination utility**: Provide a function for paginating large API responses.  
   - **Validation utility**: Centralized input validation using `Joi`.  

6. **Error Handling**:  
   - A centralized error handling middleware that provides consistent and descriptive error responses.  
   - Log all errors to the `error.log` file.  

7. **Environment Configurations**: Use a `.env` file to store sensitive credentials, including:  
   - MongoDB connection URI (`MONGO_URI`)  
   - JWT secret (`JWT_SECRET`)  
   - Email credentials (`EMAIL_USER` and `EMAIL_PASS`)  
   - Default server port (`PORT`).  

8. **API Routes**: Include:  
   - **Authentication routes** (`authRoutes.js`):  
     - `/api/auth/register`: Register a new user.  
     - `/api/auth/login`: Authenticate user and return token.  
     - `/api/auth/reset-password`: Reset user password.  
   - **User routes** (`userRoutes.js`):  
     - `/api/users/`: Get all users (admin only).  
     - `/api/users/:id`: Get user by ID.  

9. **Testing & Documentation**:  
   - Provide a Postman collection (`postman-collection.json`) for API testing.  
   - Write a `README.md` file with:  
     - Project description  
     - Installation and setup instructions  
     - API endpoint documentation.  

10. **Code Quality**: Ensure:  
    - Clean and modular code with comments explaining key logic.  
    - Following best practices for security (e.g., input sanitization, sensitive data protection).  
    - Scalability for larger projects.  

Write this project setup with all necessary files and configurations for a beginner-friendly, production-ready Node.js application."

---

This revised version ensures all aspects of the setup are covered comprehensively while being specific and actionable. You can use this prompt to regenerate the backend setup in the future or adapt it for new requirements.
