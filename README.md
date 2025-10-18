# 📝 ToDo App (Spring Boot)

A simple **To-Do List Application** built using **Spring Boot, Spring MVC, and Spring Data JPA**.  
It allows users to **add, view, toggle, and delete** tasks easily.

---

## 🚀 Features

- ➕ Create a new task  
- 📋 View all tasks  
- ✅ Mark tasks as completed / uncompleted  
- ❌ Delete tasks  
- 💾 Persistent storage using H2 / MySQL (configurable)

---

## 🧩 Project Structure


---

## ⚙️ How It Works

1. **User Interface:**  
   The front-end (`tasks.html`) interacts with the controller through HTTP requests.

2. **Controller Layer:**  
   `TaskController` maps URLs to corresponding service methods.

3. **Service Layer:**  
   `TaskService` handles logic like creating, deleting, and toggling tasks.

4. **Repository Layer:**  
   `TaskRepository` extends `JpaRepository` to manage database operations automatically.

---

## 🧱 Model Overview

| Field     | Type     | Description             |
|------------|----------|-------------------------|
| id         | Long     | Auto-generated ID       |
| title      | String   | Title of the task       |
| completed  | boolean  | Task status (true/false)|

---

## 🧭 API Endpoints

| HTTP Method | Endpoint            | Description                  |
|--------------|--------------------|------------------------------|
| `GET`        | `/`                | Display all tasks            |
| `POST`       | `/`                | Create a new task            |
| `GET`        | `/{id}/delete`     | Delete a task by ID          |
| `GET`        | `/{id}/toggle`     | Toggle a task’s completion   |

---

## 🛠️ Technologies Used

- **Spring Boot**
- **Spring MVC**
- **Spring Data JPA**
- **Thymeleaf (for UI)**
- **H2 Database** (In-memory, can be replaced with MySQL)
- **Maven** (for dependency management)
- **Java 17+**

---

## ⚙️ How to Run
## 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/ToDoApp.git
cd ToDoApp
```
## 2️⃣ Build & Run the Project

If you’re using Maven:
```bash
mvn spring-boot:run
```

or run the main class manually:
```bash
cd src/main/java/com/example/ToDoApp
java ToDoAppApplication
```

## 3️⃣ Access the App

Open your browser and go to:
```bash
http://localhost:8080/
```


## 🗃️ Database Configuration (Optional)

By default, it uses H2 in-memory DB.
To switch to MySQL, modify application.properties:

spring.datasource.url=jdbc:mysql://localhost:3306/todo_db
spring.datasource.username=root
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

## 🧰 Example Task Workflow

Enter a task title in the input box and click Add.

Click the toggle link/button to mark a task as completed.

Click delete to remove a task from the list.

## 🧑‍💻 Developer Notes

The app follows a 3-layered architecture: Controller → Service → Repository.

TaskService ensures separation of business logic from controllers.

Database operations are handled automatically by Spring Data JPA.

## 🏗️ Future Improvements

Add edit/update feature

Add user authentication (Spring Security)

Integrate with Angular frontend

Add due dates and task categories
