# CR_LAB_RECORD_TRACKER

# Lab Record & Payment Management Tool

A secure, offline-first web application built with pure JavaScript to help Class Representatives (CRs) manage lab record payments and distribution for their class.

Live Demo: lab-record-v-maan-1327.netlify.app
"""after opening the list it asks for a json file to be upload which holds the data in it.A two demo files(AIML,CSE_A) json files were available in the folder i uploaded whose passwords are AIML@1234 and CSE_A@1234 respectively"""

The Problem
A Class Representative (CR) was responsible for collecting money and distributing lab records for multiple subjects. Tracking this with spreadsheets or paper was chaotic, error-prone, and not transparent for my classmates.

The Solution
I built this tool to solve my this problem. It's an all-in-one, secure application that runs entirely in the browser, requires no internet connection after loading, and has a special two-file system:

Admin Tool (admin_tool_source.html): A private tool for the main administrator (me) to create secure, password-protected data files (.json) for each class section.

CR Tool (index.html): The public-facing tool for other CRs. They can only log in by uploading their specific encrypted file and entering their password.

All data is stored securely in the browser's localStorage and is encrypted/decrypted on the fly.

Core Features

Secure Admin Panel: Master password protection for creating new class files.

Encrypted Data Files: Uses the Web Crypto API for strong AES-GCM encryption of all class data.

Persistent Session: CRs stay logged in even after closing the browser.

Dynamic Dashboard: Real-time charts (via Chart.js) and statistics for Paid vs. Unpaid status.

Advanced Student Management:

Add, delete, and manage students.

Batch import students from Excel/CSV files (using SheetJS).

Filter students by payment status (All, Paid, Unpaid, Collected).

Detect and highlight duplicate name entries.

Select multiple students for bulk-deletion.

Customizable Labs: Full CRUD (Create, Read, Update, Delete) for lab records.

Payment & Utility Features:

UPI QR Code integration for easy payments.

Per-student note-taking.

Export filtered student lists back to an Excel file.

Tech Stack

HTML5

Tailwind CSS (for all styling)

JavaScript (ES6+) (for all application logic)

Web Crypto API: For secure encryption/decryption.

SheetJS (xlsx): For Excel file import/export.

Chart.js: For data visualization.
