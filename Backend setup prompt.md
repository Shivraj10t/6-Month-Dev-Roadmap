Certainly! Here’s a prompt you can use in the future to quickly generate this backend setup:

---

**Prompt:**

"I need a complete backend project template for a Node.js and Express-based application with the following features:  
- **Project Structure**: Follow a modular folder structure with `src/config`, `src/controllers`, `src/middlewares`, `src/models`, `src/routes`, `src/utils`, `logs`, and `public/uploads`.  
- **Database**: Use MongoDB with Mongoose. Include a robust connection setup with options like pool size and retry logic in `db.js`.  
- **Authentication & Authorization**: JWT-based login and register endpoints with role-based authorization middleware. Include email verification and password reset functionality.  
- **File Upload**: Add a middleware for file uploads (using `multer`) with storage in `public/uploads`.  
- **Utilities**: Include email utility (`nodemailer`), logging utility (`fs` and `path`), pagination utility, and validation using `Joi`.  
- **Error Handling**: Centralized error handling middleware for clean and consistent error responses.  
- **Routes**: Include `authRoutes` (register, login, reset password) and `userRoutes` (get all users, get user by ID).  
- **Environment Config**: Use `.env` file to store sensitive configurations (e.g., database URI, JWT secret, email credentials).  
- **README**: Add a `README.md` file with setup instructions.  
- **Postman Collection**: Provide a `postman-collection.json` for testing API endpoints.  

Make sure the project is structured like this:  
```
backend-template/
├── src/
│   ├── config/
│   │   ├── db.js
│   │   └── env.js
│   ├── controllers/
│   │   ├── authController.js
│   │   ├── userController.js
│   └── middlewares/
│       ├── authMiddleware.js
│       ├── roleMiddleware.js
│       ├── errorHandler.js
│       ├── fileUpload.js
│   ├── models/
│   │   ├── User.js
│   ├── routes/
│   │   ├── authRoutes.js
│   │   ├── userRoutes.js
│   ├── utils/
│       ├── email.js
│       ├── logger.js
│       ├── pagination.js
│       ├── validators.js
│   ├── app.js
│   └── server.js
├── logs/
│   ├── error.log
│   ├── combined.log
├── public/
│   └── uploads/
├── .env
├── .gitignore
├── README.md
├── package.json
├── postman-collection.json
```

Write clean, modular, and well-commented code. Follow best practices for error handling, security, and scalability. Ensure all user inputs are validated, and provide example endpoints for testing."

---
