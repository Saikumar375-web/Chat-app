# 💬 Real-Time Chat Application

A modern **full-stack real-time chat application** built using the MERN stack. The application enables users to create accounts, authenticate securely, connect with other users, and exchange messages in real time.

The project follows a client-server architecture, with a React frontend and a Node.js/Express backend connected to MongoDB. Real-time communication is handled using Socket.IO.

---

## 🚀 Features

* 🔐 User Authentication
* 📝 User Registration and Login
* 🔑 Secure password hashing using bcrypt
* 🎫 JWT-based authentication
* 💬 Real-time messaging using Socket.IO
* 👥 User management and chat functionality
* 🗄️ Persistent message storage using MongoDB
* ⚡ Fast and modern frontend built with React and Vite
* 🎨 Responsive user interface styled with Tailwind CSS
* 🔔 Toast notifications for user feedback
* 🌐 REST API integration using Axios
* ☁️ Deployment configuration using Vercel

---

## 🛠️ Tech Stack

### Frontend

* React
* Vite
* React Router DOM
* Tailwind CSS
* Axios
* Socket.IO Client
* React Hot Toast

### Backend

* Node.js
* Express.js
* MongoDB
* Mongoose
* Socket.IO
* JSON Web Token (JWT)
* bcryptjs
* Cloudinary
* CORS
* dotenv

---

## 📂 Project Structure

```text
Chat-app
│
├── client
│   ├── context
│   │   ├── AuthContext.jsx
│   │   └── ChatContext.jsx
│   │
│   ├── public
│   │
│   ├── src
│   │   ├── assets
│   │   ├── components
│   │   ├── lib
│   │   ├── pages
│   │   ├── App.jsx
│   │   ├── index.css
│   │   └── main.jsx
│   │
│   ├── package.json
│   └── vite.config.js
│
├── server
│   ├── controllers
│   │   ├── messageController.js
│   │   └── userController.js
│   │
│   ├── lib
│   ├── middleware
│   ├── models
│   │   ├── Message.js
│   │   └── User.js
│   │
│   ├── routes
│   ├── server.js
│   └── package.json
│
└── .gitignore
```

---

## ⚙️ Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/Saikumar375-web/Chat-app.git
```

Navigate to the project directory:

```bash
cd Chat-app
```

---

## 💻 Frontend Setup

Navigate to the client directory:

```bash
cd client
```

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

The frontend will typically run on:

```text
http://localhost:5173
```

---

## 🖥️ Backend Setup

Open another terminal and navigate to the server directory:

```bash
cd server
```

Install dependencies:

```bash
npm install
```

Start the server:

```bash
npm run server
```

Or run the production start command:

```bash
npm start
```

---

## 🔐 Environment Variables

Create a `.env` file inside the `server` directory and add the required environment variables.

Example:

```env
PORT=5000

MONGODB_URI=your_mongodb_connection_string

JWT_SECRET=your_jwt_secret

CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
```

> ⚠️ Never commit your `.env` file or expose API keys, database credentials, or secrets in a public repository.

---

## 🔄 Application Architecture

The application follows a typical full-stack architecture:

```text
React Client
     │
     │ HTTP Requests
     ▼
Express API
     │
     ├──────────────► MongoDB
     │                  │
     │                  ├── Users
     │                  └── Messages
     │
     ▼
Socket.IO Server
     │
     │ Real-Time Events
     ▼
Connected Users
```

---

## 💬 Real-Time Communication

The application uses **Socket.IO** to provide real-time communication between users.

Instead of repeatedly requesting the server for new messages, Socket.IO maintains a connection between the client and server, allowing messages and events to be delivered instantly.

---

## 🔑 Authentication Flow

The authentication system follows this general flow:

1. A user creates an account.
2. The password is securely hashed using `bcryptjs`.
3. User information is stored in MongoDB.
4. A JWT token is generated after successful authentication.
5. Protected routes use authentication middleware to verify the user.
6. The authenticated user can access chat functionality.

---

## 🧠 State Management

The frontend uses React Context API to manage application-level state.

### AuthContext

Responsible for managing authentication-related data and functionality, such as:

* Current user
* Authentication status
* Login
* Registration
* User session management

### ChatContext

Responsible for chat-related functionality, such as:

* Users
* Selected chat
* Messages
* Real-time updates
* Chat state

---

## 📡 API and Backend Structure

The backend follows a structured architecture:

### Controllers

Controllers contain the main application logic.

* `userController.js` handles user-related functionality.
* `messageController.js` handles messaging functionality.

### Models

MongoDB data is structured using Mongoose models.

* `User.js` manages user data.
* `Message.js` manages message data.

### Middleware

Middleware is used for functionality such as authentication and request protection.

### Routes

Routes connect API endpoints with their corresponding controllers.

---

## 📦 Available Scripts

### Client

```bash
npm run dev
```

Runs the frontend development server.

```bash
npm run build
```

Creates a production build.

```bash
npm run preview
```

Previews the production build.

```bash
npm run lint
```

Runs ESLint to check code quality.

### Server

```bash
npm run server
```

Starts the backend using Nodemon.

```bash
npm start
```

Starts the backend using Node.js.


## 👨‍💻 Author

**Sai Kumar**

GitHub: [Saikumar375-web](https://github.com/Saikumar375-web)



