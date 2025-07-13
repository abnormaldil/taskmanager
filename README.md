# 📝 Task Manager App

A full-stack Task Manager application with React frontend, Spring Boot backend, and PostgreSQL database.

![Task Manager Screenshot](https://via.placeholder.com/800x400?text=Task+Manager+Screenshot) <!-- Add your actual screenshot later -->

## ✨ Features

- ✅ Create, read, and delete tasks
- ⏰ Set deadlines and categories
- 🔄 Real-time updates
- 🛡️ Persistent data storage

## 🛠️ Tech Stack

| Frontend          | Backend         | Database       |
|-------------------|-----------------|----------------|
| React             | Spring Boot     | PostgreSQL     |
| Axios (HTTP)      | Java 21         | Hibernate JPA  |
| Material-UI       | Maven           | pgAdmin        |

## 🚀 Quick Setup

### Prerequisites

- [Node.js](https://nodejs.org/) (v16+)
- [Java JDK 21](https://adoptium.net/)
- [Maven](https://maven.apache.org/)
- [PostgreSQL](https://www.postgresql.org/) (v15+)
- [pgAdmin](https://www.pgadmin.org/) (optional)

## 🏗️ Project Structure
taskmanager/
├── taskmanager-backend/ # Spring Boot application
│ ├── src/main/java/ # Java source code
│ ├── src/main/resources/ # Config files
│ └── pom.xml # Maven config
└── taskmanager-frontend/ # React application
├── public/ # Static files
├── src/ # React components
└── package.json # NPM dependencies

text

## 🛠️ Installation

### 1. Database Setup

```sql
CREATE DATABASE taskmanagerdb;
CREATE USER taskuser WITH PASSWORD 'taskpass';
GRANT ALL PRIVILEGES ON DATABASE taskmanagerdb TO taskuser;
2. Backend Configuration
Edit taskmanager-backend/src/main/resources/application.properties:

properties
spring.datasource.url=jdbc:postgresql://localhost:5432/taskmanagerdb
spring.datasource.username=taskuser
spring.datasource.password=taskpass

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect
3. Run Backend
bash
cd taskmanager-backend
./mvnw spring-boot:run
# Or if you have Maven installed:
# mvn spring-boot:run
The backend will run at: http://localhost:8080

4. Frontend Setup
bash
cd taskmanager-frontend
npm install
npm start
The frontend will run at: http://localhost:3000

🌐 API Endpoints
Method	Endpoint	Description
GET	/api/tasks	Get all tasks
POST	/api/tasks	Create new task
DELETE	/api/tasks/{id}	Delete task by ID
🔧 Troubleshooting
Issue: Backend won't start
✅ Solution: Verify PostgreSQL is running and credentials are correct

Issue: Frontend can't connect to backend
✅ Solution: Ensure CORS is enabled in Spring Boot and backend is running

Issue: Database tables not created
✅ Solution: Check Hibernate logs and verify ddl-auto=update

🤝 Contributing
Fork the repository

Create your feature branch (git checkout -b feature/AmazingFeature)

Commit your changes (git commit -m 'Add some AmazingFeature')

Push to the branch (git push origin feature/AmazingFeature)

Open a Pull Request

📄 License
Distributed under the MIT License. See LICENSE for more information.

📧 Contact
Your Name - your.email@example.com
Project Link: https://github.com/yourusername/taskmanager

text

### Key Improvements:
1. **Better Visual Hierarchy** - Clear sections with emoji icons
2. **Tech Stack Table** - Quick overview of technologies
3. **Project Structure** - Visual tree representation
4. **Step-by-Step Setup** - Numbered instructions with code blocks
5. **Troubleshooting** - Common issues and solutions
6. **API Documentation** - Clean endpoint table
7. **Contributing Guide** - Standard GitHub workflow

You can copy this entire markdown content and paste it into your `README.md` file. Remember to:
- Replace placeholder screenshot URL with your actual app screenshot
- Update contact information
- Adjust any configuration details specific to your setup
