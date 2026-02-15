# Office-Task-Manager
A simple Office Task Manager 

1. Project Overview
The Office Task Manager is a robust, object-oriented Python application designed to streamline workplace productivity. Built using a modular architecture, the system allows for clean separation between the task logic, data modeling, and management functions.

Key Features:

OOP Architecture: Uses distinct modules (task_model, manager) for better maintainability.

Task Creation: Define tasks with specific attributes and status tracking.

Management Console: Centralized hub to view, assign, and update task progress.

Interactive Interface: A user-friendly console menu for real-time data manipulation.

2. Dependencies
This project is fully containerized, meaning the environment is pre-configured.

Primary Tool: Docker Desktop or Docker Playground.

Language: Python 3.10 (Standard Library).

Modules Included: task_manager.py (Entry Point), task_model.py, manager.py, and test_task_manager.py.

3. Installation Instructions
Clone the Repository: Ensure you have the Dockerfile and all .py files in a single directory.

No Manual Setup: You do not need to install Python or set up virtual environments locally, as the Dockerfile handles the multi-file setup using the COPY . . command.

Verify Files: Ensure the Dockerfile is in the same directory as task_manager.py.

4. Running the Project
You can execute this project instantly using the pre-built image from Docker Hub.

Run via Docker Hub:
Open your terminal and enter:

Bash
docker run -it sameshenm/office-task-manager:v1
Build and Run Locally:
If you make changes to the OOP modules, rebuild the image:

PowerShell
docker build -t office-task-manager .
docker run -it office-task-manager
5. Usage Instructions
Launch: Once the container starts, the task_manager.py script executes automatically.

Navigation: Use the numeric keypad to navigate the task management options.

Roles: Operates as a "Manager" role, allowing full CRUD (Create, Read, Update, Delete) permissions over the task list.

Testing: The test_task_manager.py file is included in the container for verifying logic integrity.

6. Additional Notes
Multi-File Handling: This project demonstrates Docker's ability to preserve Python module relationships (imports) across a containerized environment.

Standard Output: The application uses unbuffered Python mode (-u) to ensure the console output appears immediately in your terminal or Docker Playground.

Troubleshooting: If you receive a "ModuleNotFoundError," ensure you used COPY . . in your Dockerfile to include the supporting task_model.py and manager.py files.
