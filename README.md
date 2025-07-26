## Project 1: Todo-app-main

### Overview

This is a simple To-Do web application built with Flask, a Python web framework, and SQLAlchemy for database management. It allows users to add, mark as complete, and delete tasks. All tasks are stored in a SQLite database.

### Features

  * **Add Tasks**: Users can add new tasks to their To-Do list.
  * **Mark as Complete**: Tasks can be marked as completed, which visually strikes through the task.
  * **Delete Tasks**: Individual tasks can be deleted from the list.
  * **Clear All Tasks**: All tasks can be cleared from the list with a single action.
  * **Persistent Storage**: Tasks are stored in a SQLite database (`tasks.db`), ensuring they are saved even after the application is closed.

### Technologies Used

  * **Flask**: Web framework for Python.
  * **SQLAlchemy**: ORM (Object Relational Mapper) for interacting with the database.
  * **SQLite**: Lightweight, file-based database.
  * **HTML**: For the web page structure.
  * **CSS**: For styling the web application.

### Project Structure

```
Todo-app-main/
├── app.py
├── index.html
├── tasks.db
└── static/
    └── style.css
```

  * `app.py`: The main Flask application file, containing routes, database models, and logic for handling To-Do operations.
  * `index.html`: The main HTML template for the To-Do list user interface.
  * [cite\_start]`tasks.db`: The SQLite database file where tasks are stored[cite: 1].
  * `static/style.css`: (Assumed, based on `index.html` linking to `url_for('static', filename='style.css')`) This directory would contain the CSS file for styling the application, although `style.css` was not provided. The styling information found in `index.html` is embedded directly within a `<style>` tag.

### Setup and Installation

1.  **Clone the repository (or extract the zip file):**
    If you have the zip file, extract it to your desired location.

2.  **Navigate to the project directory:**

    ```bash
    cd Todo-app-main
    ```

3.  **Create a virtual environment (recommended):**

    ```bash
    python -m venv venv
    ```

4.  **Activate the virtual environment:**

      * On Windows:
        ```bash
        .\venv\Scripts\activate
        ```
      * On macOS/Linux:
        ```bash
        source venv/bin/activate
        ```

5.  **Install the required dependencies:**

    ```bash
    pip install Flask Flask-SQLAlchemy
    ```

6.  **Run the application:**

    ```bash
    python app.py
    ```

7.  **Access the application:**
    Open your web browser and go to `http://127.0.0.1:5000/`.

### Database Schema

[cite\_start]The `tasks.db` database contains a table named `task`[cite: 40]. [cite\_start]The schema for the `task` table is as follows[cite: 40]:

  * [cite\_start]`id`: `INTEGER`, Primary Key, Not Null [cite: 40]
  * [cite\_start]`content`: `VARCHAR(200)`, Not Null (stores the task description) [cite: 40]
  * [cite\_start]`completed`: `BOOLEAN` (indicates if the task is completed, default is False) [cite: 40]
