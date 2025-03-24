# task-manager-app
Task Management App-Project Explanation & Guide

A simple and interactive Task Management Application built with HTML, CSS, and JavaScript. It allows users to add, search, filter, edit, mark as completed, and delete tasks while storing data in local storage.

Features

✅ Add new tasks with a name, description, and due date.
✅ Mark tasks as completed or pending.
✅ Search tasks by name.
✅ Filter tasks: All, Pending, Completed.
✅ Delete or edit tasks.
✅ Past-due tasks are highlighted in red.
✅ Data persistence using local storage.

This document explains how to run the Task Management App, how it works, and how additional features were implemented.


---

1️⃣ How to Run the Application

🔹 Option 1: Run Locally (Open in Browser)

1. Download the project files or clone the repository:

git clone https://github.com/your-username/task-manager-app.git
cd task-manager-app


2. Locate the Task.html file.


3. Double-click to open it in any browser (Chrome, Firefox, Edge, etc.).



🔹 Option 2: Host on GitHub Pages

1. Push the project to GitHub.


2. Go to Settings > Pages in your GitHub repository.


3. Under Branch, select main and save.


4. Your app will be live at:

https://your-username.github.io/task-manager-app/


2️⃣ Project Structure & Explanation

🔸 HTML Structure (index.html)

The HTML file consists of:

1. A task input form (Task name, description, and due date).


2. A search bar to filter tasks by name.


3. Filter buttons for All, Pending, and Completed tasks.


4. A task list where tasks appear dynamically.



🔸 CSS Styling (<style> in index.html)

The design follows a clean and minimalistic UI.

Colors indicate task status (blue = pending, green = completed, red = past due).

Interactive hover effects for buttons.


🔸 JavaScript (<script> in index.html)

All logic is written in JavaScript, handling:
✅ Task addition – Adds a new task with a unique id, stores in localStorage.
✅ Task filtering – Show all, pending, or completed tasks.
✅ Task searching – Filters tasks as you type.
✅ Task completion – Marks a task as completed/pending.
✅ Task deletion – Removes a task from localStorage.
✅ Task sorting – Orders tasks by due date.
✅ Data persistence – Stores tasks in localStorage so they don’t disappear on refresh.


---

3️⃣ Step-by-Step Execution

Step 1: Add a Task

1. Enter a Task Name and Due Date.


2. Click "Add Task" → The task appears in the list.


3. Data is saved in localStorage.



Step 2: View & Filter Tasks

Click:

All → Shows all tasks.

Pending → Shows only incomplete tasks.

Completed → Shows only completed tasks.



Step 3: Search Tasks

Start typing in the search bar to filter tasks by name.


Step 4: Complete / Undo a Task

Click "Done" → Marks as completed with a green border.

Click "Undo" → Marks as pending again.


Step 5: Delete a Task

Click "Delete" → Removes the task permanently.


Step 6: Edit a Task (Future Improvement Idea)

Right now, there is an "Edit" button, but it’s not yet implemented.

It can be improved by opening an edit modal where users can modify tasks.



---

4️⃣ Additional Features Implemented

✅ 1. Past-Due Task Highlighting

If a task's due date is before today, it gets a red border to indicate urgency.

Implemented in:

const today = new Date().toISOString().split("T")[0];
const isPastDue = task.dueDate < today;
li.className = task-item ${task.completed ? "completed" : ""} ${isPastDue ? "past-due" : ""};


✅ 2. Search Bar for Real-Time Filtering

Users can search tasks by name instantly.

Implemented using:

searchInput.addEventListener("input", () => {
  renderTasks(currentFilter, searchInput.value);
});


✅ 3. Task Sorting by Due Date

Tasks are sorted automatically by due date.

Implemented using:

filteredTasks.sort((a, b) => new Date(a.dueDate) - new Date(b.dueDate));


✅ 4. Task Visibility Toggle

Click a filter button twice to hide tasks instead of just switching views.



---

5️⃣ Future Improvements (Next Steps)

🔹 Edit Task Feature – Allow users to modify existing tasks.
🔹 Dark Mode – Implement a switch for a dark theme.
🔹 Cloud Database – Replace localStorage with Firebase or MongoDB for cross-device syncing.


---
