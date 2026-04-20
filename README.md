# Full-Stack Todo List Application

This project is a full-stack Todo List application featuring a robust Java Spring Boot backend and a modern, responsive Next.js frontend. 

## Project Structure

The repository contains two main directories:

- `TodoListJavaSpring`: The backend REST API powered by Java 24, Spring Boot 3.5, and PostgreSQL.
- `todolistnext`: The frontend user interface built with Next.js 15, React 19, TypeScript, and TailwindCSS.

## Technologies Used

**Frontend (`todolistnext`)**
- Next.js 15 (App Router)
- React 19
- TypeScript
- TailwindCSS 4

**Backend (`TodoListJavaSpring`)**
- Java 24
- Spring Boot 3.5.5
- Spring Data JPA
- PostgreSQL
- Lombok
- Maven Wrapper

---

## Prerequisites

Before running the project, ensure you have the following installed:
- **Java 24** (or compatible JDK)
- **Node.js** (v20+ recommended) and **npm**
- **PostgreSQL**

---

## Getting Started

Follow the steps below to set up and run both the backend and frontend locally.

### 1. Database Setup

The backend requires a PostgreSQL database to run.

1. Ensure your PostgreSQL server is running.
2. Create a new database named `todo_db`.
3. The default backend configuration connects with these credentials (defined in `TodoListJavaSpring/src/main/resources/application.properties`):
   - **URL:** `jdbc:postgresql://localhost:5432/todo_db`
   - **Username:** `postgres`
   - **Password:** `1234`

*(If your credentials differ, make sure to update the `application.properties` file in the backend directory).*

### 2. Backend Setup (Java Spring Boot)

Navigate to the backend directory and start the Spring Boot application using the provided Maven wrapper (no local Maven installation required):

```bash
cd TodoListJavaSpring
```

**On Linux/macOS:**
```bash
chmod +x mvnw
./mvnw spring-boot:run
```

**On Windows:**
```cmd
mvnw.cmd spring-boot:run
```

The backend server will start and typically run on `http://localhost:8080`.

### 3. Frontend Setup (Next.js)

Open a new terminal window, navigate to the frontend directory, install dependencies, and start the development server:

```bash
cd todolistnext
npm install
npm run dev
```

The frontend application will start and be available at `http://localhost:3000`.

---

## Notes

- Make sure both the backend and frontend servers are running simultaneously for the application to function correctly.
- The frontend connects to the backend API. If the backend is running on a different port than `8080`, ensure you update the API service endpoints in the frontend code (`todolistnext/services/todoService.ts`).
