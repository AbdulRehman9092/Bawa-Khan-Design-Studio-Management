# Bawa Khan Design Studio Management

This is a real-time, multi-user task management application designed for the Bawa Khan Design Studio. It provides separate, feature-rich dashboards for employees and a comprehensive overview dashboard for the owner, enabling efficient project tracking and team monitoring. The entire application is built within a single `index.html` file, leveraging modern frontend technologies for a dynamic user experience.

## Key Features

*   **Multi-User Dashboards**: Separate, authenticated views for the studio owner and multiple employees (Abuzar, Kamran, Maqbool, Ali Zulfiqar, Mudassir, Ali, Abdul Rehman).
*   **Real-time Task Management**: Tasks are synchronized in real-time across all users using Firebase.
    *   **Add, Edit, & Delete Tasks**: Full CRUD functionality for tasks, including name, description, deadline, and revision counts.
    *   **Task Status Views**: Employee dashboards are organized into `Today's Tasks`, `Active Tasks`, and `Tasks Done` for clear workflow management.
    *   **Payment Tracking**: track payment status (`Paid`, `Not Paid`, `Don't Know`) and amount for each task.
*   **Owner's Overview**: A centralized dashboard for the owner (Sir Atif Bawa) to view all tasks assigned to all employees.
*   **Employee Status**: Employees can set their status to `FREE` or `BUSY`, which is visible to the owner.
*   **Global Search**: The owner can search for any task by name or description across all employees and task categories.
*   **Responsive Design**: A modern, clean, and responsive UI built with Tailwind CSS that works on all device sizes.

## Technology Stack

*   **Frontend**: HTML5, CSS3, JavaScript (ES6+)
*   **UI Framework**: [Tailwind CSS](https://tailwindcss.com/)
*   **JavaScript Library**: [Alpine.js](https://alpinejs.dev/)
*   **Backend & Database**: [Firebase Realtime Database](https://firebase.google.com/docs/database)
*   **Icons**: [Font Awesome](https://fontawesome.com/)
*   **Animations**: [Animate.css](https://animate.style/)

## Setup and Installation

To run this project locally, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/AbdulRehman9092/Bawa-Khan-Design-Studio-Management.git
    cd Bawa-Khan-Design-Studio-Management
    ```

2.  **Configure Firebase:**
    *   Go to the [Firebase Console](https://console.firebase.google.com/) and create a new project.
    *   In your project, create a new **Realtime Database**. Start in test mode for easy setup (or configure security rules for production).
    *   Copy your Realtime Database URL. It will look something like `https://your-project-name-default-rtdb.firebaseio.com`.
    *   Open the `index.html` file and find the following line (around line 3010):
        ```javascript
        const API_URL = 'https://task-manager-global-default-rtdb.firebaseio.com';
        ```
    *   Replace the placeholder URL with your own Firebase Realtime Database URL.

3.  **Run the application:**
    *   Simply open the `index.html` file in your web browser. For best results and to avoid any potential CORS issues, it's recommended to serve the file using a local web server (e.g., VS Code's Live Server extension).

## How to Use

1.  **User Selection**: Upon opening the application, you will be prompted to select a user. Click on a user's name to access their dashboard.
2.  **Employee Dashboard**:
    *   Use the tabs to switch between `Today's Tasks`, `Active Tasks`, and `Tasks Done`.
    *   In the `Active Tasks` tab, add new tasks using the "ADD TASK" button. You can edit task details directly on the task cards.
    *   Select tasks from the active list to add to your `Today's Tasks` list.
    *   Mark tasks as complete, send them back for revision, or delete them.
    *   Toggle your availability status (`FREE`/`BUSY`) using the button in the header.
3.  **Owner Dashboard**:
    *   View tasks for all employees, categorized by their current status (`Today`, `Active`, `Done`).
    *   See the real-time availability of each employee.
    *   Use the search bar at the top to find specific tasks across the entire system.
    *   Directly edit task details, including deadlines, payments, and revisions, for any employee.
