# 📝 Task Manager App

A minimal yet powerful full-stack **Task Manager** where users can add, view, and delete tasks with categories and deadlines.

Built with:
- ⚛️ React (Frontend)
- 🌱 Spring Boot (Backend)
- 🐘 PostgreSQL (Database)

---

## 📁 Project Structure

taskmanager/
├── taskmanager-backend/ # Spring Boot project
└── taskmanager-frontend/ # React frontend


## ⚙️ Requirements

Ensure the following tools are installed on your system:

- [Node.js](https://nodejs.org/) (v16+ recommended)
- [Java JDK 21](https://adoptium.net/)
- [Maven](https://maven.apache.org/) (or use the wrapper `./mvnw`)
- [PostgreSQL](https://www.postgresql.org/) (port 5432)
- [pgAdmin](https://www.pgadmin.org/) (optional, for GUI DB access)

---

## 🧱 Backend Setup (Spring Boot)

### Step 1: Create Database

Open **pgAdmin** or use CLI to create a database:
CREATE DATABASE taskmanagerdb;

### Step 2: Configure Database in application.properties
Edit taskmanager-backend/src/main/resources/application.properties:

#### properties:
spring.datasource.url=jdbc:postgresql://localhost:5432/taskmanagerdb
spring.datasource.username=your_postgres_username
spring.datasource.password=your_postgres_password
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect

### Step 3: Run the Backend
#### bash:
cd taskmanager-backend
./mvnw spring-boot:run   # or mvn spring-boot:run if Maven is installed
The backend API will be live at:
http://localhost:8080

## 🌐 Frontend Setup (React)
### Step 1: Navigate to frontend folder
bash:
cd taskmanager-frontend
### Step 2: Install dependencies
bash:
npm install
### Step 3: Start the React app
bash:
npm start

The frontend will run at:
http://localhost:3000

Make sure the backend is running on localhost:8080.

### 📡 Backend API Endpoints
Method	Endpoint	Description
GET	/api/tasks	Fetch all tasks
POST	/api/tasks	Add new task
DELETE	/api/tasks/{id}	Delete task by ID

### 🔒 Notes
CORS is enabled in the backend to allow frontend access at http://localhost:3000

Data is stored persistently in PostgreSQL

Spring Boot auto-generates the database schema based on your entity

### 📄 License
This project is open-source and available under the MIT License
