# 📸 SnapTrack - Smart Attendance System

Developed a web-based attendance system using facial recognition for my B.Tech Minor Project. Students register with selfie videos, and teachers upload class recordings. The system automatically detects and marks attendance based on facial recognition, streamlining the process and improving accuracy.

## 🚀 Features

- 📚 Role-based login system (Admin / Teacher / Student)
- 🎥 Upload & manage videos for class attendance
- 🧠 Face recognition using deep learning embeddings
- 📊 Dashboard and attendance analytics
- 🔐 Secure login sessions
- 💾 Swappable database backend (SQLite ➜ PostgreSQL-ready)

---

### ⚙️ Setup Instructions

## 1. 📦 Install Requirements

pip install -r requirements.txt

## 2. ⚙️ Create .env file
Create a .env file in the root folder and add your configuration:

SECRET_KEY=your-secret-key
SQLALCHEMY_DATABASE_URI=sqlite:///../instance/app.db
UPLOAD_FOLDER=app/static/uploads/
ADMIN_ID=adminid
ADMIN_PASSWORD=adminpassword
⚠️ This file is ignored by Git for security.

## 3. 🗂️ Create Initial Database (Development)
If you're running the app for the first time or made changes to models, use the helper script to create tables:

python helper/create_tables.py

## 4. ▶️ Run the Application

python run.py

The app will be accessible at:
http://localhost:5000

💡 Notes
.gitkeep files are placed inside empty folders like uploads/ to ensure directory structure is preserved in Git.

instance/app.db (the SQLite DB file) is ignored via .gitignore. Anyone can create their own DB.

Uploaded media like class and student videos are not stored. They should be uploaded by users.


📦 Coming Soon

✅ Flask-Migrate integration

🌐 PostgreSQL config

☁️ Deployment guide (Render/Heroku)

📈 Advanced analytics and attendance summaries