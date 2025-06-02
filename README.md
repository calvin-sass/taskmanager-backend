# Task Manager Backend API

A robust RESTful API built with Express.js and MongoDB to power a task management application. This backend provides authentication, user management, task management, and reporting features.

## Features

- **Authentication System**: Secure login and registration with JWT
- **User Management**: Create, update, and manage user profiles
- **Task Management**: Create, read, update, and delete tasks
- **File Uploads**: Support for file attachments
- **Reporting**: Generate reports with Excel export capability

## Technologies

- Node.js
- Express.js (v5.1.0)
- MongoDB (via Mongoose v8.15.0)
- JSON Web Tokens (JWT) for authentication
- bcryptjs for password hashing
- multer for file uploads
- exceljs for report generation

## Installation

1. Clone the repository
2. Install dependencies:
   ```
   npm install
   ```
3. Create a `.env` file in the root directory with the following variables:
   ```
   NODE_ENV=development
   PORT=5000
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret
   CLIENT_URL=http://localhost:3000
   ```
4. Start the development server:
   ```
   npm run dev
   ```

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register a new user
- `POST /api/auth/login` - Login and get authentication token

### Users
- `GET /api/users` - Get all users (admin)
- `GET /api/users/:id` - Get user by ID
- `PUT /api/users/:id` - Update user
- `DELETE /api/users/:id` - Delete user

### Tasks
- `GET /api/tasks` - Get all tasks
- `GET /api/tasks/:id` - Get task by ID
- `POST /api/tasks` - Create a new task
- `PUT /api/tasks/:id` - Update a task
- `DELETE /api/tasks/:id` - Delete a task

### Reports
- `GET /api/reports` - Generate reports based on tasks

## Project Structure

```
backend/
├── config/        # Database configuration
├── controllers/   # Route controllers (logic)
├── middlewares/   # Express middlewares
├── models/        # Mongoose models
├── routes/        # Route definitions
├── uploads/       # User uploaded files
└── server.js      # Express app entry point
```

## Development

Start the development server with:

```
npm run dev
```

## Deployment

This project is configured for deployment on Vercel with a `vercel.json` configuration file.

## License

ISC
