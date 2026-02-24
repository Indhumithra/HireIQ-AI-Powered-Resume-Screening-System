
# 🤖 HireIQ — AI-Powered Resume Screening System

> An intelligent Applicant Tracking System (ATS) powered by Semantic AI and NLP.

---

## 📌 Overview

HireIQ is an AI-driven resume screening system that evaluates candidate resumes using semantic similarity instead of traditional keyword matching. It converts resumes and job descriptions into dense vector embeddings using SBERT and calculates a weighted Fit Score based on skills, experience, and education.

---

## ✨ Features

* 📄 Resume parsing (.pdf, .docx, .txt)
* 🧠 Semantic similarity matching (SBERT)
* 📊 Weighted AI Fit Score calculation
* 📝 Explainable AI rationale generation
* 📧 Automated shortlist email notifications
* 🌗 Light/Dark mode dashboard
* 📈 Interactive data visualization (Chart.js)
* 🧪 Integration testing using Pytest

---

## 🏗️ Tech Stack

### Backend

* Python
* Flask
* SQLite (SQLAlchemy ORM)
* sentence-transformers (all-mpnet-base-v2)
* PyTorch
* spaCy
* pdfplumber
* python-docx
* pandas, numpy

### Frontend

* HTML5
* CSS3
* JavaScript
* Chart.js
* Jinja2 Templates

---

## 🧠 How It Works

1. HR uploads resumes.
2. System extracts text using pdfplumber / python-docx.
3. spaCy performs Named Entity Recognition (NER).
4. SBERT converts resume & job description into embeddings.
5. Cosine similarity calculates semantic alignment.
6. Weighted ranking engine generates Fit Score.
7. Shortlisted candidates receive automated email.

---

## 📂 Project Structure

```
resume_screener/
│
├── app/
│   ├── routes/
│   ├── services/
│   ├── utils/
│   ├── models.py
│   ├── config.py
│   └── database.py
│
├── tests/
├── uploads/
├── instance/
├── run.py
├── requirements.txt
└── README.md
```

---

## 🚀 Installation

### 1️⃣ Clone Repository

```bash
git clone https://github.com/your-username/hireiq.git
cd hireiq
```

### 2️⃣ Create Virtual Environment

```bash
python -m venv venv
venv\Scripts\activate   # Windows
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ Configure Environment Variables

Create `.env` file:

```
SECRET_KEY=your-secret-key
MAIL_SERVER=smtp.gmail.com
MAIL_PORT=587
MAIL_USE_TLS=true
MAIL_USERNAME=your-email@gmail.com
MAIL_PASSWORD=your-app-password
```

### 5️⃣ Run Application

```bash
python run.py
```

Open:

```
http://localhost:5000
```

---

## 🔐 Default Admin Login

Username: `admin`
Password: `admin`

---

## 🧪 Run Tests

```bash
pytest tests/ -v
```

---

## 📧 Email Notification

When a candidate status is changed to **shortlisted**, the system automatically sends an email using SMTP configuration.

---

## 🗺️ Future Improvements

* PostgreSQL + pgvector integration
* Background workers using Celery
* LLM-based AI summarization
* Multi-tenant enterprise deployment

---

## 👩‍💻 Author

**Indhumithra M**
BE Computer Science Engineering
