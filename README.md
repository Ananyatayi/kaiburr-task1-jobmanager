# 🧩 Job Manager REST API

### 📘 Overview
The **Job Manager REST API** is a Spring Boot application that manages executable shell commands as “tasks.”  
Each task can be created, viewed, searched, deleted, and executed, with results stored in a MongoDB database.  
This project demonstrates a clean backend service with RESTful endpoints and task execution tracking.

---

### ⚙️ Tech Stack
| Component | Technology |
|------------|-------------|
| Language | Java 21 |
| Framework | Spring Boot 3 |
| Database | MongoDB |
| Build Tool | Maven |
| Testing | Postman / cURL |

---
### 🚀 How to Run
1. **Start MongoDB**
   docker run -d --name mongo_jobmgr -p 27020:27017 mongo:6
2.Run the application
    set APP_MONGO_URI=mongodb://localhost:27020/jobmanagerdb
    mvn spring-boot:run
3. The server will be available at http://localhost:8085

| Method   | Endpoint                      | Description             |
| -------- | ----------------------------- | ----------------------- |
| `GET`    | `/v1/tasks`                   | Retrieve all tasks      |
| `GET`    | `/v1/tasks?id={id}`           | Retrieve task by ID     |
| `GET`    | `/v1/tasks/find?name={query}` | Search task by name     |
| `PUT`    | `/v1/tasks`                   | Create or update a task |
| `PUT`    | `/v1/tasks/{id}/execution`    | Execute a task command  |
| `DELETE` | `/v1/tasks/{id}`              | Delete a task by ID     |


Features

Create, view, search, and delete tasks.

Execute shell commands safely and store outputs.

Maintain execution history with timestamps.

MongoDB persistence for all task data.
