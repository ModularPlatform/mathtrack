# Student Math Score Management Application

## Overview
The **Student Math Score Management Application** is designed to streamline exam management, grading, and score tracking for students, teachers, and administrators.  
It features an **administrator web interface** and a **student mobile app** (Android/iOS), enabling:
- Digital exam answer submissions
- Automated grading with weighted scoring
- Score history tracking and trend visualization
- Community board for student communication

---

## Objectives
- Register and manage answer sheets per exam.
- Allow students or teachers to submit answers digitally.
- Auto-compare answers with correct responses and apply weight-based scoring.
- Provide per-question accuracy, total scores, and detailed analytics.
- Support future expansion into **AI-based answer sheet scanning** and **visual dashboards**.

---

## Key Features

| Feature Category | Feature Name | Description |
|------------------|--------------|-------------|
| **Answer Sheet** | Register | Admins register correct answers and question weights based on exam metadata. |
| **Answer Submission** | Submit | Users select the exam (date, grade, etc.) and submit answers digitally. |
| **Auto-Grading** | Compare & Grade | System matches answers, applies weights, and calculates scores. |
| **Results** | View Score | Displays per-question accuracy, total scores, and correct answers. |
| **Administration** | Manage Data | Manage users, answer sheets, and submissions (edit/delete supported). |
| **Community** | Student Board | Students can view and post messages (announcements, Q&A, study tips). |

---

## System Architecture

### 1. Administrator Web Page
- Pre-register answer sheets (correct answers & weights).
- Input standard score tables and percentile charts.
- View and edit student submissions.
- Trigger automated grading.
- Responsive UI (PC/tablet support).
- Secure admin-only access.

### 2. Database System 
- Stores:
  - Answer sheets
  - Student submissions
  - Scoring results
  - User accounts & roles  
- Indexed for fast retrieval.

### 3. Server & Backend Logic
- **API:** RESTful endpoints for web and mobile clients.
- **Auth:** JWT-based authentication.
- **Logic:** Answer matching, score calculation, error handling.
- **Backend Options:** Node.js (Express) / Django REST Framework / FastAPI.

### 4. Mobile Application (Student Client)
- Secure login (Google, Facebook, Apple, Kakao supported).
- View score history, trends, and per-question results.
- Student board for Q&A and announcements.

### 5. Authentication & Roles
- **Admins:** Full access to all data.
- **Teachers:** View/manage their own students' data.
- **Students:** View personal scores, post in board.
- Role-based access control.

---
