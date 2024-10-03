# E-Notes Project – Real-Time Project

## Overview

E-Notes is a comprehensive note and task management application developed using Spring Boot for the backend and Angular/React for the frontend. It provides robust features for user authentication, notes organization, and task management, including search, export, and reminders, making it a perfect tool for users looking to keep their notes and tasks organized.

---

## Technology Stack

### Backend:
- **Spring Boot REST**
- **JPA** (Java Persistence API)
- **AOP** (Aspect-Oriented Programming)
- **Logging** (SLF4J/Logback)
- **Spring Boot Actuator**
- **Spring Security** (OAuth Login)
- **Caching** (EhCache/Redis)
- **Junit & Mockito** (Unit Testing)
- **SonarQube** (Code Quality and Analysis)
- **JMeter** (Performance Testing)
- **Swagger** (API Documentation)
- **Spring Schedulers** (Task Scheduling)
- **Docker** (Containerization)
- **GitHub** (Version Control)

### Frontend:
- **Angular** or **React** (Your choice of frontend framework)

### Database:
- **MySQL** (Relational Database)

### Tools:
- **GitHub** (Source Code Management)
- **STS** (Spring Tool Suite)
- **Figma** (UI/UX Design)

### Deployment:
- **AWS** (Amazon Web Services)

---

## Functionality & Features

### 1. **User Authentication and Authorization**
- **User Registration**: Users can register using their email, with email verification for account activation.
- **User Login**: JWT-based token authentication is used to secure user sessions.
- **Role-based Access Control**: Features are accessible based on user roles (Admin, User).

### 2. **Notes Management**
- **Category Management**: Users can create, update, and delete categories for notes organization.
- **Notes Management**: 
  - Create, edit, and delete notes.
  - Attach files to notes (PDF, images, etc.) and view/download them.
  - Paginated view of notes for easier navigation.
  - Search functionality (by title, content, category, etc.).
  - Mark notes as favorite and view a list of favorite notes.
  - **Copy Notes**: Easily duplicate notes.
  - **Export Notes**: Export all notes or single notes in Excel or PDF format.

### 3. **To-Do Management**
- **Task Management**:
  - Create, edit, and delete tasks.
  - Assign priority levels to tasks (Low, Medium, High).
  - Track task statuses (e.g., "To-Do", "In Progress", "Completed").
  - Set reminders for tasks with push notifications and email reminders.

---

## Getting Started

### Prerequisites
- Java 11+
- Node.js (for frontend development)
- MySQL (database setup)
- Docker (optional, for containerization)

### Backend Setup
1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/e-notes-project.git
    ```
2. Navigate to the backend directory and run the application:
    ```bash
    cd e-notes-backend
    ./mvnw spring-boot:run
    ```

### Frontend Setup (Angular/React)
1. Install dependencies:
    ```bash
    npm install
    ```
2. Run the frontend application:
    ```bash
    npm start
    ```

### Database Setup
1. Create a MySQL database:
    ```sql
    CREATE DATABASE enotes_db;
    ```
2. Update the database credentials in the application properties.

### Running Tests
- Use JUnit and Mockito for unit tests:
    ```bash
    ./mvnw test
    ```
- Use JMeter for performance testing.

---

## API Documentation
- Access the API documentation using **Swagger** at:
    ```
    http://localhost:8080/swagger-ui.html
    ```

---

## Deployment

### Docker Setup
- Build and run the application using Docker:
    ```bash
    docker-compose up --build
    ```

### AWS Deployment
- Use AWS EC2 or AWS Elastic Beanstalk for deployment. Ensure environment variables are set for production.

---

## License
This project is licensed under the MIT License - see the LICENSE file for details.

