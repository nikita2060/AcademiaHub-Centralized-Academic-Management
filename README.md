# AcademiaHub – Centralized Academic Management

This is a Node.js-based school management system with role-based authentication using Express, MongoDB, and JWT.

## Features

- User authentication with JWT
- Role-based access control (Student ,Teacher,Admin)
- Secure password handling
- MongoDB integration with Mongoose
- Frontend integration support

## Technologies Used

- Node.js
- Express.js
- MongoDB & Mongoose
- JWT (JSON Web Token) for authentication
- bcrypt.js for password hashing
- dotenv for environment variables
- CORS support

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/your-username/school-management-system.git
   cd school-management-system
   ```

2. Install dependencies:
   ```sh
   npm install --legacy-peer-deps
   ```

3. Set up environment variables:
   Create a `.env` file in the root directory and add the following:
   ```env
   JWT_SECRET=your_jwt_secret
   ```

4. Start MongoDB (if not running):
   ```sh
   mongod
   ```

5. Run the server:
   ```sh
   node server.js
   ```

## API Endpoints

### Authentication

#### Login
- **Endpoint:** `POST /login`
- **Request Body:**
  ```json
  {
    "email": "user@example.com",
    "password": "yourpassword"
  }
  ```
- **Response:**
  ```json
  {
    "token": "your_jwt_token",
    "role": "student"
  }
  ```

### Protected Routes

#### Student Dashboard
- **Endpoint:** `GET /student-dashboard`
- **Headers:**
  ```
  Authorization: Bearer your_jwt_token
  ```
- **Response:**
  ```json
  {
    "message": "Welcome to Student Dashboard"
  }
  ```

#### Teacher Dashboard
- **Endpoint:** `GET /teacher-dashboard`
- **Headers:**
  ```
  Authorization: Bearer your_jwt_token
  ```
- **Response:**
  ```json
  {
    "message": "Welcome to Teacher Dashboard"
  }
  ```

## Project Structure
```
school-management-system/
│── api/                # Backend API logic
│── frontend/           # Frontend code
│── models/
│   └── user.model.js   # User schema for authentication
│── node_modules/       # Node.js dependencies
│── .env                # Environment variables
│── .gitignore          # Ignored files
│── package.json        # Dependencies & scripts
│── server.js           # Main entry point
│── public/
│── src/
│── Admission.html      # Frontend HTML files
│── login.html
│── mail.png            # Assets
│── Portal.html
│── TimeTable.html
│── valid.js            # Frontend validation script
```

## License

This project is open-source and available under the [MIT License](LICENSE).

