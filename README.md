# simple-authorisation-api
🛡️ Secure Authentication API with JWT (Node.js + Express + MongoDB)
This project is a simple and secure backend authentication API that allows users to:

✅ Register with username, email, and password

✅ Login using email and password

✅ Access protected profile route using JWT (JSON Web Token)

📁 Folder Structure
pgsql
Copy
Edit
.
├── middleware/
│   └── verifyToken.js       # Middleware to protect private routes
├── models/
│   └── User.js              # Mongoose User schema
├── routes/
│   └── auth.js              # Auth routes (register, login, profile)
├── .env                     # Environment variables (Mongo URI, JWT secret)
├── server.js                # Entry point of the server
└── README.md
🚀 Getting Started
1️⃣ Clone the project
bash

git clone https://github.com/your-username/auth-api.git
cd auth-api
2️⃣ Install dependencies
bash

npm install
3️⃣ Create .env file
Create a .env file in the root directory and add:

env

PORT=3000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
Replace the values with your actual MongoDB URI and a strong secret key.

4️⃣ Run the server
bash
Copy
Edit
node server.js
✅ You should see:

arduino
Copy
Edit
MongoDB connected
Server running on port 3000
🧪 API Endpoints
🔹 Register
POST /api/register

json
Copy
Edit
{
  "username": "ananya",
  "email": "ananya@gmail.com",
  "password": "test1234"
}
✅ Response:

json
Copy
Edit
{
  "message": "User registered",
  "userId": "6439abcde12345"
}
🔹 Login
POST /api/login

json
Copy
Edit
{
  "email": "ananya@gmail.com",
  "password": "test1234"
}
✅ Response:

json
Copy
Edit
{
  "token": "JWT_TOKEN_HERE",
  "username": "ananya"
}
🔹 Get Profile (Protected)
GET /api/profile

Add Authorization header:

makefile
Copy
Edit
Authorization: Bearer YOUR_TOKEN_HERE
✅ Response:

json
Copy
Edit
{
  "_id": "6439abcde12345",
  "username": "ananya",
  "email": "ananya@gmail.com"
}
❌ If token is missing or invalid:

json
Copy
Edit
{
  "error": "Access Denied" // or "Invalid Token"
}
🔧 Technologies Used
Node.js

Express.js

MongoDB + Mongoose

bcryptjs for password hashing

jsonwebtoken (JWT) for secure authentication

dotenv for environment variables

CORS for cross-origin requests

