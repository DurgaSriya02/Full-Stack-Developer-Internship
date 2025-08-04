# Full-Stack-Developer-Internship

Intern Project Dashboard
This project is a simple web application designed to demonstrate a basic client-server architecture. It features a frontend dashboard that fetches data from a separate Java-based backend.

Features
User Dashboard: Displays an intern's name, referral code, and total donations raised.

Leaderboard: Shows a ranked list of interns based on their donation amounts.

Page Navigation: Allows seamless switching between the dashboard and leaderboard views.

Simulated Backend: The backend provides mock data to the frontend through a REST API.

Technologies Used
Frontend:

HTML5, CSS3, JavaScript (for all user interface and logic).

Backend:

Java (version 17 or higher).

Spring Boot (a framework for building Java applications).

Maven (a build automation and project management tool).

Getting Started
To run this project, you need to set up both the backend and the frontend.

1. Backend Setup (Java)
The backend provides the data for the frontend. It is built using Spring Boot and managed by Maven.

Prerequisites:

Java Development Kit (JDK) 17 or higher.

Maven installed on your machine.

Instructions:

Create the project directory:

mkdir intern-project
cd intern-project

Create the Maven configuration file: Save the provided pom.xml file inside this directory. This file is crucial because it tells Maven which libraries (like Spring Boot) to download for your project.

Create the source code directory:

mkdir -p src/main/java/com/example/internprojectbackend

Save the Java source code: Save the provided InternProjectBackendApplication.java file in the directory you just created.

Run the server: Open a terminal in your project's root directory (where pom.xml is located) and execute the following Maven command. Maven will automatically download all dependencies and start the server.

mvn spring-boot:run

Note: The server will typically run on http://localhost:8080.

2. Frontend Setup (HTML, CSS, JS)
The frontend is a single HTML file that fetches data from the running backend.

Instructions:

Save the HTML file: Save the provided intern-project.html file anywhere on your computer.

Open in a browser: Open the file in your preferred web browser (e.g., Chrome, Firefox).

How It Works
The Java backend runs as a server, exposing two API endpoints: /api/dashboard and /api/leaderboard.

The intern-project.html file runs in your browser.

When you log in, the JavaScript in the HTML file sends a fetch request to the backend at http://localhost:8080/api/dashboard to get the user's information.

When you click "View Leaderboard", another fetch request is sent to http://localhost:8080/api/leaderboard.

The backend returns the data as JSON, and the frontend updates the page content accordingly.

Important Note: The frontend and backend are two separate applications. The frontend will not work correctly unless the Java backend server is running in the background.
