# deeper-test
# Deeper App

This project consists of a Flask backend and a Vue frontend. Follow the instructions below to set up and run both parts of the application.

---

## Backend Setup (Flask + MongoDB)

### Prerequisites
- Python 3.x installed
- MongoDB installed and running on `mongodb://localhost:27017/`
- `pip` package manager installed

### Install Dependencies
Navigate to the backend directory and install the required Python dependencies:
```sh
pip install flask pymongo dataclasses
```

### Run the Flask Server
Start the backend server by running:
```sh
python app.py
```
The API will be available at `http://127.0.0.1:5000/`.

---

## Frontend Setup (Vue.js + Vite)

### Prerequisites
- Node.js installed (preferably latest LTS version)
- npm (comes with Node.js)

### Install Dependencies
Navigate to the frontend directory and install the required dependencies:
```sh
npm install
```

### Run the Vue App
To start the development server, run:
```sh
npm run dev
```
This will start the Vue application at `http://localhost:5173/` (default Vite port).

### Build for Production
To generate a production build, run:
```sh
npm run build
```

### Preview Production Build
To preview the production build locally, run:
```sh
npm run preview
```

---

## Project Structure

```
/deeper-test
│── server/   # Flask backend
│── client/  # Vue frontend
```

Make sure both backend and frontend are running to use the full functionality of the application.

---

## API Endpoints (Backend)
- `GET /users` - Retrieve all users
- `GET /user/<username>` - Retrieve a specific user
- `POST /user` - Create a new user
- `PUT /user/<username>` - Update user information
- `DELETE /user/<username>` - Delete a user

---

## Tech Stack
- **Backend:** Flask, MongoDB, pymongo
- **Frontend:** Vue 3, Vue Router, PrimeVue, Axios, Vite
