# 📸 SnapTrack - Smart Attendance System

A smart attendance system leveraging the power of facial recognition to streamline and automate attendance tracking. Students register effortlessly with selfie videos, and teachers simply upload class recordings. SnapTrack intelligently detects faces, accurately marks attendance, and offers a fast, accurate, and completely hands-free solution!

---

## ✨ Key Features

* **Role-Based Access:** Secure and distinct login portals for Administrators, Teachers, and Students, ensuring appropriate access levels.
* **Effortless Video Management:** Teachers can easily upload and manage class recordings for attendance processing.
* **Intelligent Face Recognition:** Built upon robust deep learning models for accurate and reliable facial detection and recognition.
* **Comprehensive Analytics Dashboard:** Gain valuable insights with attendance analytics presented in an intuitive dashboard.
* **Secure Session Handling:** Robust session management to protect user data and maintain application security.
* **Seamless Database Migrations:** Integrated Flask-Migrate for smooth and efficient database schema updates.
* **Flexible Database Choice:** Easily switch between the simplicity of SQLite for development and the power of PostgreSQL for production by a simple configuration change.

---

## 🛠️ Getting Started

Follow these straightforward steps to get SnapTrack up and running on your local machine:

### Prerequisites

* **Python:** Ensure you have Python 3.8 or a later version installed on your system. 
* **Git:** Git is required to clone the repository. If you don't have it.

### Installation Steps

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/samdarshi-git/smart_attendance_system.git](https://github.com/samdarshi-git/smart_attendance_system.git)
    cd smart_attendance_system
    ```

2.  **Install Dependencies:**
    Navigate to the cloned directory and install the necessary Python packages:
    ```bash
    pip install -r requirements.txt
    ```

3.  **Configure Environment Variables:**
    Create a `.env` file in the root directory of the project and populate it with your specific configurations:
    ```ini
    SECRET_KEY=your-secret-key-here
    SQLALCHEMY_DATABASE_URI=sqlite:///../instance/app.db
    UPLOAD_FOLDER=app/static/uploads/
    ADMIN_ID=your-admin-id
    ADMIN_PASSWORD=your-admin-password
    ```
    **Note:** To use PostgreSQL, modify the `SQLALCHEMY_DATABASE_URI` to your PostgreSQL connection string. For example: `postgresql://user:password@host:port/database_name`.

4.  **Initialize and Migrate the Database:**
    Use Flask-Migrate to set up the database:
    ```bash
    flask db init      # Run this only for the first time
    flask db migrate -m "Initial migration"
    flask db upgrade
    ```

5.  **Launch the Application:**
    Start the Flask development server:
    ```bash
    python run.py
    ```
    You can now access the application in your web browser at `http://localhost:5000`.

6.  **Admin Login:**
    Use the `ADMIN_ID` and `ADMIN_PASSWORD` you defined in the `.env` file to log in to the Admin dashboard and start managing your system.

---

## 📂 Project Structure

smart_attendance_system/
├── app/
│   ├── init.py
│   ├── models.py         # Database models
│   ├── forms.py          # Form definitions
│   ├── routes/           # Application routes and views
│   ├── ml/               # Machine learning related code
│   ├── static/uploads/   # Directory for uploaded videos
│   └── templates/        # HTML templates
├── helper/
│   └── create_tables.py  # Optional script for initial database setup (dev/testing)
├── instance/
│   └── app.db            # SQLite database file (default)
├── migrations/         # Database migration scripts
├── run.py              # Application entry point
├── .env                # Environment variables
├── .gitignore          # Specifies intentionally untracked files that Git should ignore
├── requirements.txt    # List of Python dependencies
└── README.md           # This file


---

## 🚀 What's On the Horizon?

* **🌐 PostgreSQL Integration Ready:** Seamlessly switch to a production-ready PostgreSQL database with a simple `.env` configuration.
* **🚀 Deployment Guide:** Stay tuned for comprehensive deployment guides for popular platforms like Heroku and Render.
* **📈 Enhanced Analytics:** Expect more detailed attendance analytics and insightful visual representations.
* **🔁 CI/CD and Testing:** We are working on implementing Continuous Integration/Continuous Deployment pipelines and robust testing frameworks.

---

## ❤️ Made with Love by Samdarshi