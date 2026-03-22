# AI-Based Multimodal Tuberculosis Detection System

A complete end-to-end system for TB screening, using a combination of deep learning for Chest X-Ray images and machine learning for clinical tabular data. This application features a modern 3D React user interface with glassmorphism aesthetics, driven by a robust local FastAPI backend.

## Features
- **Multimodal AI Analysis**: Combines a Convolutional Neural Network (TensorFlow MobileNet simulation) for X-Rays and a clinical rule-based/ML engine for symptom data.
- **3D Interactive Interface**: Built with React Three Fiber, providing a premium healthcare dashboard experience.
- **Explainable AI (Mock)**: Visual representation highlighting affected X-Ray areas using Grad-CAM approximations.
- **Automated PDF Reports**: Generates detailed medical PDF reports upon diagnosis.
- **Email Notifications**: Automatically emails reports to doctors using dynamic SMTP configs.
- **Secure Authentication**: JWT-based login/signup for secure medical record access.

## How to Run Locally

### 1. Backend (FastAPI)
The backend uses Python 3.10+ and requires a virtual environment.
1. Open a terminal and navigate to the `backend/` directory:
   ```cmd
   cd backend
   .\venv\Scripts\activate
   ```
2. Run the FastAPI server:
   ```cmd
   python run.py
   ```
   *The API will start at `http://localhost:8000`*

### 2. Frontend (React + Vite)
The frontend requires Node.js (LTS).
1. Open a new terminal and navigate to the `frontend/` directory:
   ```cmd
   cd frontend
   ```
2. Start the Vite React development server:
   ```cmd
   npm run dev
   ```
   *The UI will start at `http://localhost:5173` (or the port specified by Vite).*

### 3. Usage Guide
- Open `http://localhost:5173`.
- Click "Sign Up" to create a test doctor account.
- Log in and navigate to the Dashboard.
- Go to "New Diagnosis" in the sidebar.
- Upload any Chest X-Ray test image, toggle the clinical parameters, and click "Run Diagnostics".
- A comprehensive TB risk profile will be generated, the report saved to `backend/reports/`, and a simulated email sent.

## Technologies Used
- **Frontend**: React, Vite, TailwindCSS, React Three Fiber, Framer Motion, Recharts
- **Backend**: Python, FastAPI, SQLAlchemy (SQLite), Passlib/pyJWT, TensorFlow (Keras), FPDF
