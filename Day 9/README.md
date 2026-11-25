# FastAPI – Student Management API 🚀

A beginner-friendly REST API built using **FastAPI** and Python to perform CRUD (Create, Read, Update, Delete) operations on student records.

This project demonstrates how to build API endpoints using different HTTP methods such as GET, POST, PUT, PATCH, and DELETE.

## 🚀 Features

- Retrieve all student records
- Retrieve a student using their ID
- Add new student records
- Update complete student details
- Update individual student information
- Delete student records
- Automatic API documentation using Swagger UI

## 🛠️ Technologies Used

- Python
- FastAPI
- Uvicorn

## 📂 Project Structure

```text
FastAPI-Student-Management/
│
├── main.py
└── README.md
```

## ⚙️ Installation and Setup

### 1. Clone the Repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
```

### 2. Navigate to the Project Directory

```bash
cd FastAPI-Student-Management
```

### 3. Create a Virtual Environment

```bash
py -m venv venv
```

### 4. Activate the Virtual Environment

**Windows:**

```bash
venv\Scripts\activate
```

### 5. Install Dependencies

```bash
pip install fastapi uvicorn
```

### 6. Run the Application

```bash
uvicorn main:app --reload
```

The application will run at:

```text
http://127.0.0.1:8000
```

## 📌 API Endpoints

| HTTP Method | Endpoint | Description |
|---|---|---|
| GET | `/students` | Get all students |
| GET | `/students/{id}` | Get student by ID |
| POST | `/students` | Add a new student |
| PUT | `/students/{id}` | Update complete student details |
| PATCH | `/students/{id}` | Update student age |
| DELETE | `/students/{id}` | Delete a student |

## 🔍 API Operations

### 1. GET – Retrieve All Students

```http
GET /students
```

Returns the list of all available students.

### 2. GET – Retrieve Student by ID

```http
GET /students/1
```

Returns the student details matching the specified ID.

### 3. POST – Add a New Student

```http
POST /students?id=3&name=Kumar&age=22
```

Adds a new student record to the student list.

### 4. PUT – Update Student Details

```http
PUT /students/1?name=Immanuel&age=23
```

Updates the complete student details for the specified ID.

### 5. PATCH – Update Student Age

```http
PATCH /students/1?age=24
```

Updates only the age of the specified student.

### 6. DELETE – Delete Student

```http
DELETE /students/1
```

Deletes the student record matching the specified ID.

## 📖 API Documentation

FastAPI automatically generates interactive API documentation.

After starting the application, open:

**Swagger UI:**

http://127.0.0.1:8000/docs

**ReDoc:**

http://127.0.0.1:8000/redoc

You can test all the API endpoints directly through Swagger UI.

## 💡 Sample Student Data

```python
students = [
    {"id": 1, "name": "Imman", "age": 22},
    {"id": 2, "name": "Arun", "age": 21}
]
```

## 🎯 Learning Outcomes

- Understood the fundamentals of FastAPI.
- Learned how to create REST API endpoints.
- Practiced GET, POST, PUT, PATCH, and DELETE methods.
- Learned how to use path parameters and query parameters.
- Implemented basic CRUD operations.
- Explored automatic API documentation using Swagger UI.

## 🔮 Future Enhancements

- Integrate a database such as SQLite or MySQL.
- Implement Pydantic models for request validation.
- Add proper HTTP status codes and exception handling.
- Implement student search and filtering.
- Add authentication and authorization.

## 👨‍💻 Author

**Immanuel**

GitHub: [FastAPI-Student-Management](https://github.com/Immanuelimman123/FastAPI-Student-Management)

---

⭐ Learning Python, APIs, and Generative AI – One Project at a Time!
