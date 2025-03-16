# deeper-test
# User Management System

This project consists of a **Flask** backend with **MongoDB** and a **Vue.js** frontend for managing users. The backend provides a REST API for user operations, and the frontend consumes these APIs.

---

## 🛠 Prerequisites

Make sure you have the following installed:

- Python 3.8+
- Node.js 16+
- npm or yarn
- MongoDB (running on `localhost:27017`)

---

## 🔧 Backend Setup (Flask & MongoDB)

### 1️⃣ Install dependencies
```sh
pip install -r requirements.txt
```

### 2️⃣ Start MongoDB
Ensure MongoDB is running locally on port `27017`.
If using Docker, run:
```sh
docker run -d --name mongodb -p 27017:27017 mongo
```

### 3️⃣ Run the backend
```sh
python app.py
```

The backend should now be running at `http://127.0.0.1:5000`.

---

## 🖥 Frontend Setup (Vue.js)

### 1️⃣ Navigate to the frontend directory
```sh
cd frontend
```

### 2️⃣ Install dependencies
```sh
npm install
```

### 3️⃣ Start the Vue development server
```sh
npm run dev
```

The frontend should now be accessible at `http://localhost:5173`.

---

## 📌 API Endpoints

### 🔹 Get All Users
```http
GET /users
```
**Response:**
```json
[
  {
    "username": "john_doe",
    "roles": ["admin"],
    "timezone": "UTC",
    "active": true,
    "created_ts": 1672531200,
    "last_updated": "N/A"
  }
]
```

### 🔹 Get a Single User
```http
GET /user/{username}
```

### 🔹 Create a User
```http
POST /user
```
**Body:**
```json
{
  "username": "john_doe",
  "password": "securepassword",
  "roles": ["admin"],
  "preferences": { "timezone": "UTC" }
}
```

### 🔹 Update a User
```http
PUT /user/{username}
```

### 🔹 Delete a User
```http
DELETE /user/{username}
```

---

## 🎯 Import Sample Data

As soon as you run the Flask application, the data will be imported to Database.

---

## 🚀 Running Both Backend & Frontend

To run both the backend and frontend simultaneously:
1. Open a terminal and start the backend: `python app.py`
2. Open another terminal, navigate to `frontend/`, and start Vue: `npm run dev`

Your Vue.js app should now be connected to your Flask API!

---

## 🎉 Done!

Now you have a working **Flask + Vue.js** user management system! If you run into any issues, feel free to debug using:
```sh
# Check for errors in the backend
python app.py

# Check for Vue errors
npm run dev
```
