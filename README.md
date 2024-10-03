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
