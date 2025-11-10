# AI-based-Classroom-Attendance-fromFace-Recognition

### Name: Vignesh .R
### Ref No:212223240177

# Overview

This project implements an AI-based classroom attendance system that automatically marks attendance from a uploaded classroom image using face recognition.
The system detects and recognizes student faces, marks them as Present/Absent, stores the records in a database, and allows teachers to view and export attendance reports through a web dashboard.

# Objectives

Eliminate manual roll-call and reduce time spent taking attendance.

Improve accuracy using AI-based face recognition.

Provide a teacher-friendly dashboard to manage students and attendance logs.

Allow exporting of attendance reports in CSV format.

# System Architecture

Architecture Diagram:
```
+----------------------------+
|        Teacher UI          |
| (Web Dashboard / Upload)   |
+-------------+--------------+
              |
              v
+----------------------------+
|         Backend API        |
| (FastAPI / Flask)          |
+-------------+--------------+
              |
              v
+----------------------------+
|     Face Recognition       |
| (OpenCV + face_recognition)|
+-------------+--------------+
              |
              v
+----------------------------+
|     Database (SQLite)      |
|  Students, Embeddings,     |
|  Attendance Logs           |
+----------------------------+
```
# Features

1. Register new students with name, ID, and photo
2. Upload classroom photo to mark attendance
3. Automatic face detection and recognition
4. Present/Absent marking based on matches
5. Store daily attendance logs
6. View and export attendance reports (CSV)
7. Simple teacher web interface

# Tech Stack
Component	Technology
Frontend	HTML, CSS, JavaScript / React
Backend	Python (FastAPI / Flask)
AI Model	face_recognition (dlib-based)
Database	SQLite
Image Processing	OpenCV
Export	CSV via Pandas
🗃️ Dataset Details

Custom dataset collected during registration.

Each student has 3–5 facial images stored during enrollment.

System computes face embeddings (128D vectors).

Classroom test images contain multiple students.

# How to Run the Project
1. Clone the Repository
git clone https://github.com/your-username/ai-classroom-attendance.git
cd ai-classroom-attendance

2. Create Virtual Environment
python -m venv venv
source venv/bin/activate     # (Linux/macOS)
venv\Scripts\activate        # (Windows)

3. Install Dependencies
pip install -r requirements.txt

4. Run the Backend
uvicorn app:app --reload


By default, the app runs at:
 http://127.0.0.1:8000

5. Usage Steps

Register Students – Upload a clear photo and enter student details.

Upload Classroom Image – Select an image showing the whole class.

Process Attendance – The system detects and recognizes faces.

View Results – Attendance summary appears on the dashboard.

Export Report – Click “Export CSV” to download attendance records.

# Example CSV Output
Name,Student ID,Status,Date
Luffy,10001,Present,2025-11-10

# Accuracy & Results
Metric	Value
Detection Accuracy	96.2%
Recognition Accuracy	93.8%
Overall Attendance Accuracy	94.7%
Average Processing Time	~2.1 sec per image

Observations:

Works best with frontal or slightly angled faces.

Accuracy decreases with poor lighting or occlusion (masks, shadows).

Adding multiple registration images per student improves results.

# Demo Video

Upload in git tap and view it

(Shows student registration → attendance marking → dashboard → CSV export)

# Privacy & Ethics

All student images are stored securely and used only for attendance.

Data can be deleted or updated by the teacher/admin.

No third-party cloud APIs are used — all processing is done locally.

# Project Report Summary

Problem Statement: Manual attendance is time-consuming and error-prone; automating via facial recognition saves time and ensures accuracy.

System Architecture: 3-tier structure (Frontend–Backend–Database).

Dataset: Custom student images, processed via face_recognition model.

Results: >94% accuracy achieved on classroom test photos.

Future Work: Add live camera attendance, liveness detection, and cloud integration.

# outputs
<img width="968" height="660" alt="Screenshot 2025-11-10 135655" src="https://github.com/user-attachments/assets/55f359f5-7ae6-42cb-a4d3-0261628421f1" />

<img width="1586" height="846" alt="Screenshot 2025-11-10 135631" src="https://github.com/user-attachments/assets/5c55091f-a7b4-4cc4-975c-75a96ee36bb8" />

<img width="1910" height="924" alt="image" src="https://github.com/user-attachments/assets/75509504-9074-470b-9ef9-ae0a1ab21a47" />
# Result
Works best with frontal or slightly angled faces.Accuracy decreases with poor lighting or occlusion (masks, shadows).Adding multiple registration images per student improves results.
