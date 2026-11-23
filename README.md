# AuthFlow 🔐

**A simple full-stack authentication application built with React and Flask.**

AuthFlow is a learning project that demonstrates how a React frontend communicates with a Flask backend to implement user registration, login, JWT-based authentication, and protected routes.

## ✨ Features

- **User Registration:** Create an account with a username and password.
- **User Login:** Authenticate using registered credentials.
- **JWT Authentication:** Generate and use JSON Web Tokens for authenticated requests.
- **Protected Routes:** Restrict dashboard access to authenticated users.
- **Session Management:** Store and manage authentication tokens using browser LocalStorage.
- **Logout:** Clear the authentication token and end the local session.

## 🛠️ Tech Stack

| Frontend | Backend |
|---|---|
| React | Python |
| JavaScript (JSX) | Flask |
| Vite | Flask-JWT-Extended |
| React Router | Flask-CORS |
| LocalStorage | Python-dotenv |

## 📁 Project Structure

```text
AuthFlow/
│
├── backend/
│   └── app.py
│
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   │   └── ProtectedRoute.jsx
│   │   ├── context/
│   │   │   └── AuthContext.jsx
│   │   ├── pages/
│   │   │   ├── Dashboard.jsx
│   │   │   ├── Login.jsx
│   │   │   └── Register.jsx
│   │   ├── App.jsx
│   │   └── main.jsx
│   └── package.json
│
├── requirements.txt
└── Procfile
```

## ⚙️ Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/israemakkour/AuthFlow.git
cd AuthFlow
```

### 2. Set up the backend

Create and activate a Python virtual environment:

```bash
python -m venv venv
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

Start the Flask server:

```bash
python backend/app.py
```

The backend runs on:

`http://127.0.0.1:5000`

### 3. Set up the frontend

Open another terminal:

```bash
cd frontend
npm install
```

Start the development server:

```bash
npm run dev
```

For production, build the frontend:

```bash
npm run build
```

The generated frontend build is served by the Flask application.

## 🔄 Application Flow

1. A user registers with a username and password.
2. The backend stores the registration information.
3. The user logs in with their credentials.
4. Flask generates a JWT access token.
5. React stores the token in LocalStorage.
6. The token is sent with requests to protected endpoints.
7. The user can access the dashboard and log out.

## ⚠️ Current Limitations

This project is an educational prototype, not a production-ready authentication system.

- User accounts are stored in an in-memory Python list, so they are lost when the backend restarts.
- Passwords are currently stored as plain text.
- The JWT secret has a development fallback and should be configured securely through environment variables.
- The application uses a local backend URL for API requests.

These limitations would need to be addressed before deploying the application for real users.

## 🎯 Purpose

This project explores the fundamentals of full-stack web development, API communication, user authentication, and frontend/backend integration.
