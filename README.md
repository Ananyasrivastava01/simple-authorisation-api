# simple-authorisation-api
🛡️ Secure Authentication API with JWT (Node.js + Express + MongoDB)
This project is a simple and secure backend authentication API that allows users to:

✅ Register with username, email, and password

✅ Login using email and password

✅ Access protected profile route using JWT (JSON Web Token)


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
PORT=3000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
Replace the values with your actual MongoDB URI and a strong secret key.

4️⃣ Run the server

node server.js

MongoDB connected
Server running on port 3000
🧪 API Endpoints
🔹 Register
POST /api/register
🔹 Login
POST /api/login
🔹 Get Profile (Protected)
GET /api/profile

Add Authorization header:
Authorization: Bearer YOUR_TOKEN_HERE

🔧 Technologies Used
Node.js
Express.js
MongoDB + Mongoose
bcryptjs for password hashing
jsonwebtoken (JWT) for secure authentication
dotenv for environment variables
CORS for cross-origin requests

