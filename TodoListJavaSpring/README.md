# TodoListJavaSpring

A Spring Boot application for managing a Todo List, built with Java 24, Spring Boot 3.5, and PostgreSQL.

## Prerequisites

Before you begin, ensure you have the following installed:
- **Java 24** (or compatible JDK)
- **PostgreSQL**

## Database Configuration

This application requires a PostgreSQL database to run. 

1. Ensure your PostgreSQL server is running.
2. Create a database named `todo_db`.
3. The default configuration connects with the following credentials (defined in `src/main/resources/application.properties`):
   - **URL:** `jdbc:postgresql://localhost:5432/todo_db`
   - **Username:** `postgres`
   - **Password:** `1234`

If your database configuration differs, update the `application.properties` file accordingly.

## How to Run (Without an IDE)

Yes, you can run this application entirely from the command line (or here in Antigravity) without needing an IDE like Eclipse or IntelliJ! 

This project uses the Maven Wrapper (`mvnw`), which means you don't even need to have Maven installed on your system. The wrapper will automatically download the correct version of Maven for you.

### 1. Open a Terminal
Navigate to the root directory of the project (where this `README.md` and `pom.xml` are located).

### 2. Make the Wrapper Executable (Linux/macOS only)
If you are on Linux or macOS, you might need to make the Maven wrapper script executable first:
```bash
chmod +x mvnw
```

### 3. Run the Application
Execute the following command to start the Spring Boot server:

**On Linux/macOS:**
```bash
./mvnw spring-boot:run
```

**On Windows:**
```cmd
mvnw.cmd spring-boot:run
```

### 4. Access the Application
Once the application starts, you should see the Spring Boot banner and log output in your terminal. By default, it will be running on `http://localhost:8080`.

## Building the Application

If you want to package the application into a standalone runnable JAR file, you can run:

**On Linux/macOS:**
```bash
./mvnw clean package
```

**On Windows:**
```cmd
mvnw.cmd clean package
```

This will create a `.jar` file in the `target/` directory, which you can run using standard Java:
```bash
java -jar target/TodoListJavaSpring-0.0.1-SNAPSHOT.jar
```
