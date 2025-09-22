🗓️ CSE Timetable Scheduler – PHP & MySQL Based System
🔍 Overview
The CSE Timetable Scheduler is a web-based automation tool that dynamically generates weekly academic timetables for the Computer Science & Engineering Department. Built using PHP, MySQL, and hosted on a XAMPP local server, it simplifies scheduling by respecting subject limits, avoiding repetition, and ensuring a balanced distribution of classes.

📌 Features
📚 Auto-assigns theory subjects based on selected semester

🔄 Respects the max_per_week limit set for each subject

🔁 Avoids subject repetition in the same day

🍽️ Automatically schedules a lunch break in a random mid-day period

🧾 Generates timetables for multiple sections (A, B, C)

📊 Displays data in a clean, styled HTML table

🛠️ Admin panel to manage:

Teachers

Subjects

Classrooms

Allotments

🏗️ Tech Stack
Component	Technology
Backend	PHP
Database	MySQL
Frontend	HTML, CSS, Bootstrap
Server	XAMPP (Apache + MySQL)

🧮 Database Schema Highlights
Table: subjects

Column	Description
subject_code	Unique code for each subject
subject_name	Name of the subject
semester	Semester number (3-8)
max_per_week	Max lectures per week allowed

Additional Tables:

teachers

classrooms

subject_allotments, etc.

⚙️ Timetable Logic
Iterates over 6 weekdays and 8 daily periods

Assigns a random lunch break each day (excluding first period)

Tracks how many times each subject is used with a counter

Prevents repeating the same subject within one day

Fills remaining unassigned periods with -

🧪 How to Run Locally (XAMPP)
✅ Install XAMPP from apachefriends.org

🗂️ Place the project folder in C:\xampp\htdocs\ (or your htdocs directory)

🗄️ Open phpMyAdmin (http://localhost/phpmyadmin) and create a database named ttms

📥 Import the SQL dump (manually or via import tab)

⚙️ Ensure database config in PHP:

php
Copy
Edit
$conn = new mysqli("localhost", "root", "", "ttms");
▶️ Start Apache and MySQL from the XAMPP Control Panel

🌐 Open your browser and go to:
http://localhost/<your-folder-name>/generatetimetable.php

📅 Select the desired semester and click VIEW TIMETABLE

📁 Folder Structure
bash
Copy
Edit
/ttms/
├── addteachers.php
├── addsubjects.php
├── addclassrooms.php
├── allotsubjects.php
├── allotpracticals.php
├── allotclasses.php
├── generatetimetable.php  <-- core generation logic
├── assets/
│   ├── css/
│   └── js/
├── index.php
└── ...
📈 Future Enhancements
📚 Add practical/lab session support
🔄 Add teacher preferences / availability constraints
🧠 Integrate optimization algorithms for smarter scheduling
📤 Export timetable as PDF/Excel

👤 Author
Aryan Tiwari
GitHub: @ryan171807
Email: aryan1tiwari71807@gmail.com

