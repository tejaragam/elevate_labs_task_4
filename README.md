1. Prepare Your Project Folder
Your folder structure should look like this:

flask_users_api/
│
├── app.py              # Your Flask CRUD application code
├── requirements.txt    # Dependencies
└── README.md           # Theory/Explanation (this is what will be visible on GitHub)
2. Save Your Code in app.py
app.py is the code you already wrote.

3. Create requirements.txt
    Flask==3.0.2
4. Create a README.md File for Theory
Here’s a sample theory write‑up you can put in your README.md file to submit on GitHub.

README.md
text
# Flask Users REST API

## 📌 Objective
The aim of this project is to demonstrate the fundamentals of REST API development using **Python** and **Flask**, with in-memory data storage.

---

## ⚙️ Tools & Technologies
- **Python 3.x**
- **Flask Framework**
- **Postman** or `curl` for testing

---

## 📖 Theory

### 1. **What is a REST API?**
REST (Representational State Transfer) is an architectural style used for designing networked applications.  
It uses HTTP methods (`GET`, `POST`, `PUT`, `DELETE`) to perform CRUD operations on resources.

---

### 2. **API Endpoints**
Our API manages "Users" using five CRUD routes:

| HTTP Method | Endpoint            | Description                   |
|-------------|---------------------|-------------------------------|
| GET         | `/users`            | Fetch all users               |
| GET         | `/users/<id>`       | Fetch a single user by ID     |
| POST        | `/users`            | Create a new user             |
| PUT         | `/users/<id>`       | Update an existing user       |
| DELETE      | `/users/<id>`       | Delete a user by ID           |

---

### 3. **In-memory Data Storage**
- We use a Python dictionary `users = {}` to store user data.
- Each user has:
{
"id": int,
"name": "string",
"email": "string"
}

text
- All data is lost when the server restarts (since it's stored in RAM).

---

### 4. **Flow of Operations**
1. **POST /users** → Add a new user with name & email.
2. **GET /users** → Retrieve all user records.
3. **GET /users/<id>** → Retrieve specific user details.
4. **PUT /users/<id>** → Update details of an existing user.
5. **DELETE /users/<id>** → Remove a user.

---

### 5. **Running the Application**
1. Create a virtual environment:
python -m venv venv

text
2. Activate it:
venv\Scripts\activate

text
3. Install dependencies:
pip install -r requirements.txt

text
4. Run the server:
python app.py

text
5. The API will be running at:
http://127.0.0.1:5000/

text

---

### 6. **Testing**
#### Using Postman:
- Set method (GET/POST/PUT/DELETE)
- Enter endpoint
- Send request

#### Using curl:
Example for creating a user:
curl -X POST http://127.0.0.1:5000/users ^
-H "Content-Type: application/json" ^
-d "{"name":"Alice", "email":"alice@example.com"}"

text

---

## 🚀 Outcome
This project covers:
- Setting up a Flask application
- Implementing REST API routes
- Handling JSON request/response
- Using HTTP methods for CRUD operations

---

## 📌 Limitations
- Data is not persistent (use DB in future)
- No authentication/authorization yet

---
5. Push to GitHub
Initialize Git in project folder:

bash
git init
Add files:

bash
git add .
Commit changes:

bash
git commit -m "Initial commit - Flask Users API with theory"
Create repo on GitHub (via website).

Link remote repo:

bash
git remote add origin https://github.com/your-username/flask_users_api.git
Push code:

bash
git branch -M main
git push -u origin main
Now your GitHub repository will contain:

The Flask API code

The theory/readme explanation

The requirements.txt file

