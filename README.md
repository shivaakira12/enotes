# E-Notes Project – Real-Time Project

A comprehensive note-taking and task management application, offering a rich feature set with user authentication, notes organization, and to-do management. This project is designed for personal and professional note-taking needs with seamless file attachments, categorization, and task prioritization.

## Technology Stack

### Backend:
- **Framework**: Spring Boot (REST API)
- **Persistence**: JPA (Java Persistence API)
- **Other Tools**:
  - Aspect-Oriented Programming (AOP)
  - Logging (Spring Boot Actuator)
  - Security (OAuth 2.0, JWT)
  - Caching (e.g., Redis or Ehcache)
  - Testing: Junit & Mockito
  - Code Quality: SonarQube
  - Performance Testing: JMeter
  - API Documentation: Swagger
  - Scheduling Tasks: Spring Schedular
  - Containerization: Docker
  - Version Control: GitHub

### Frontend:
- **Framework**: Angular / React

### Database:
- **DBMS**: MySQL

### Development Tools:
- **GitHub** (for version control)
- **Spring Tool Suite (STS)** (for backend development)
- **Figma** (for UI/UX design)

### Deployment:
- **Server**: AWS (Amazon Web Services)

---

## Functionality & Features

### User Authentication and Authorization:
- **User Registration**: Includes email verification for security.
- **User Login**: JWT-based token authentication system.
- **Role-Based Access Control**: Different roles with specific access (e.g., Admin, User).

### Notes Management:
- **Category Management**:
  - Create, update, and delete categories.
  - Filter notes by category.
- **Notes Operations**:
  - Create, edit, and delete notes.
  - Attach files (PDF, images, etc.) to notes.
  - View or download attached files.
  - Search for notes based on title, content, or category.
  - Paginated view for managing large sets of notes.
  - Mark notes as favorites and view favorite notes in a separate list.
  - Copy notes for easy duplication.
  - Export notes to Excel or PDF (single or bulk export).

### Todo Management:
- **Task Operations**:
  - Create, edit, and delete tasks.
  - Assign priority levels (Low, Medium, High) to tasks.
  - Set task statuses like "To-Do", "In Progress", and "Completed".
- **Reminders**:
  - Set reminders for tasks with push notifications and email alerts.

---

## How to Run the Project

### Prerequisites:
- Java 8+
- Node.js (for Angular or React)
- MySQL
- Docker (optional, for containerized deployment)

### Backend Setup:
1. Clone the repository from GitHub.
2. Open the project in Spring Tool Suite (STS).
3. Configure MySQL database settings in the `application.properties` file.
4. Run the Spring Boot application.

### Frontend Setup:
1. Navigate to the frontend directory (Angular or React).
2. Install the required dependencies:
   ```bash
   npm install
   ```

---

## Database Setup

To set up the database for the E-Notes project, execute the following SQL commands in your MySQL database environment. These commands will create the necessary tables for users, roles, categories, notes, file details, and todos.

### SQL Commands

1. **Create Users Table**
   ```sql
   CREATE TABLE users (
       id INT AUTO_INCREMENT PRIMARY KEY,
       first_name VARCHAR(100) NOT NULL,
       last_name VARCHAR(100) NOT NULL,
       email VARCHAR(255) NOT NULL UNIQUE,
       password VARCHAR(255) NOT NULL,
       mobile_no VARCHAR(15)
   );
   ```

2. **Create Role Table**
   ```sql
   CREATE TABLE role (
       id INT AUTO_INCREMENT PRIMARY KEY,
       name VARCHAR(100) NOT NULL
   );
   ```

3. **Create User_Role Table**
   ```sql
   CREATE TABLE user_role (
       id INT AUTO_INCREMENT PRIMARY KEY,
       user_id INT NOT NULL,
       role_id INT NOT NULL,
       FOREIGN KEY (user_id) REFERENCES users(id) ON DELETE CASCADE,
       FOREIGN KEY (role_id) REFERENCES role(id) ON DELETE CASCADE
   );
   ```

4. **Create Category Table**
   ```sql
   CREATE TABLE category (
       id INT AUTO_INCREMENT PRIMARY KEY,
       name VARCHAR(255) NOT NULL,
       is_active BOOLEAN DEFAULT TRUE,
       is_deleted BOOLEAN DEFAULT FALSE,
       created_by INT,
       created_on TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
       updated_by INT,
       updated_on TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP NOT NULL
   );
   ```

5. **Create Notes Table**
   ```sql
   CREATE TABLE notes (
       id INT AUTO_INCREMENT PRIMARY KEY,
       title VARCHAR(1000) NOT NULL,
       description VARCHAR(1000),
       category_id INT,
       file_id INT NULL,
       created_by INT,
       created_on TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
       updated_on TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
   );
   ```

6. **Create File_Details Table**
   ```sql
   CREATE TABLE file_details (
       id INT AUTO_INCREMENT PRIMARY KEY,
       original_file_name VARCHAR(255) NOT NULL,
       display_file_name VARCHAR(255) NOT NULL,
       upload_file_name VARCHAR(255) NOT NULL,
       path VARCHAR(500) NOT NULL,
       file_size DOUBLE NOT NULL,
       file_type VARCHAR(100) NOT NULL
   );
   ```

7. **Create Todo Table**
   ```sql
   CREATE TABLE todo (
       id INT AUTO_INCREMENT PRIMARY KEY,
       title VARCHAR(255) NOT NULL,
       description VARCHAR(1000),
       priority INT,
       status INT,
       created_by INT,
       created_on TIMESTAMP DEFAULT CURRENT_TIMESTAMP
   );
   ```

### Notes
- Make sure to configure your MySQL connection settings in the `application.properties` file before running the Spring Boot application.
- Ensure that you have MySQL installed and running on your local machine or server.
```

This README includes a detailed overview of the project, technology stack, functionality, and instructions for running the project, along with the database setup section. If you have any other requirements or need further adjustments, feel free to let me know!
