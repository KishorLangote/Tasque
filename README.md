# Tasque

A full-stack Todo Management App that helps users create, view, update, and delete todos. It allows users to keep track of their daily goals or activities, mark them as completed & remove them once done. 
Built with React frontend, Express/Node, MongoDB database and JWT-based authentication.

---

## Demo Link

[Live Demo](https://frontend-tasquee.vercel.app/login)

---


## Quick start

```
git clone https://github.com/KishorLangote/Tasque.git
cd backend
npm install
npm run dev

cd frontend
npm install
npm run dev

```

---

## Technologies
- React JS
- Tailwind CSS
- React Router
- Node JS
- Express
- MongoDB

---

## Demo Video
[Loom Video]()

---


## Features

**Home**
- Displays all tasks individually, you can add or delete todos or mark them as completed.
- Instantly add new todos to your to-do list.
- Easily toggle tasks between completed and pending status.
- Remove todos from the list when no longer needed.
- Todos are saved using localStorage.

**Authentication**
- User signup and login with JWT.
- Protected routes for see the other users task and home.

---
## API Reference

### **POST /api/v1/user/signup**<br>
Register new user<br>
```
request: 

{
    "username": "Kunal",
    "email": "kunal@gmail.com",
    "password": "kunal@123"
}

response: 

[
  {
    "message": "User registered successfully",
    "newUser": {
        "username": "Kunal",
        "email": "kunal@gmail.com",
        "password": "$2b$10$MB7N.iudey4.kPmokFRob.FeHOapjM971U/aFxafhHK301ye2gqB6",
        "_id": "6863cd027d7a506038a5a73f",
        "createdAt": "2025-07-01T11:56:50.977Z",
        "updatedAt": "2025-07-01T11:56:50.977Z",
        "__v": 0
    },
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiI2ODYzY2QwMjdkN2E1MDYwMzhhNWE3M2YiLCJpYXQiOjE3NTEzNzEwMTAsImV4cCI6MTc1MjIzNTAxMH0.4GCkUobG6pThqApZ7OITH8UGsMAXJ6ZY6h4tlCDcBYM"
 }
]
```

### **POST /api/v1/user/login**<br>

```
request: 

{
    "email": "kunal@gmail.com",
    "password": "kunal@123"
}

response:

[
  {
    "message": "User logged in successfully",
    "user": {
        "_id": "6863cd027d7a506038a5a73f",
        "username": "Kunal",
        "email": "kunal@gmail.com",
        "password": "$2b$10$MB7N.iudey4.kPmokFRob.FeHOapjM971U/aFxafhHK301ye2gqB6",
        "createdAt": "2025-07-01T11:56:50.977Z",
        "updatedAt": "2025-07-01T11:56:50.997Z",
        "__v": 0,
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiI2ODYzY2QwMjdkN2E1MDYwMzhhNWE3M2YiLCJpYXQiOjE3NTEzNzEwMTAsImV4cCI6MTc1MjIzNTAxMH0.4GCkUobG6pThqApZ7OITH8UGsMAXJ6ZY6h4tlCDcBYM"
    },
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiI2ODYzY2QwMjdkN2E1MDYwMzhhNWE3M2YiLCJpYXQiOjE3NTEzNzExODUsImV4cCI6MTc1MjIzNTE4NX0.mFkiFyB7Q0SCF10Hqoh2P8pjCyWnnBTX7mvGQQLUphA"
}
]

```
### **GET /api/v1/user/logout**<br> 

### **GET /api/v1/todo/fetch**<br>
List all todos<br>
```
response:

[
  {
    "message": "Todo Fetched Successfully",
    "todos": [
        {
            "_id": "6861f69560c56d09df344cb7",
            "text": "todo5",
            "completed": false,
            "user": "6861f59460c56d09df344cab",
            "createdAt": "2025-06-30T02:29:41.111Z",
            "updatedAt": "2025-06-30T03:03:38.575Z",
            "__v": 0
        }
    ]
}
]

```
### **POST /api/v1/todo/create**<br>
create todos<br>
```
request:

  {
    "text": "Go for walk",
    "completed": true
  }

response:

[ 
  {
    "message": "Todo Created Successfully",
    "newTodo": {
        "text": "Go for walk",
        "completed": true,
        "user": "6861f59460c56d09df344cab",
        "_id": "6863c9357d7a506038a5a733",
        "createdAt": "2025-07-01T11:40:37.116Z",
        "updatedAt": "2025-07-01T11:40:37.116Z",
        "__v": 0
    }
 }
]


```

### **PUT /api/v1/todo/update/:todoId**<br>
Update todo<br>
```
request:

{
    "text": "Go for walk",
    "completed": false
}

response: 

[
  {
    "message": "Todo updated Successfully",
    "todo": {
        "_id": "6863c9357d7a506038a5a733",
        "text": "Go for walk",
        "completed": false,
        "user": "6861f59460c56d09df344cab",
        "createdAt": "2025-07-01T11:40:37.116Z",
        "updatedAt": "2025-07-01T11:48:37.037Z",
        "__v": 0
    }
 }
]
```
### **DELETE /api/v1/todo/delete/:todoId**<br>
Delete todo<br>
```
response: 

[
  {
    "message": "Todo deleted Successfully",
    "todo": {
        "_id": "6862637957d28171e15cb168",
        "text": "todo5-3",
        "completed": true,
        "user": "6861f59460c56d09df344cab",
        "createdAt": "2025-06-30T10:14:17.430Z",
        "updatedAt": "2025-06-30T10:14:17.430Z",
        "__v": 0
    }
  }
]

```
---

## Contact
For bugs or feature request, please react out to kishorlangote2@gmail.com

