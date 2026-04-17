# 🏥 HealthCare Portal — Django Capstone Project

A comprehensive **Healthcare Management System** built with Django covering:
- Patient Management & Medical Records
- Doctor Profiles & Specializations
- Appointment Booking & Scheduling
- Pharmacy & Inventory Management
- Role-based User Authentication

---

## 📁 Project Structure

```
healthcare_project/
├── manage.py
├── requirements.txt
├── setup.py                  ← Run this to populate sample data
├── healthcare_project/       ← Django project settings
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── accounts/                 ← User auth, roles, profiles
├── patients/                 ← Patient records, vitals, medical history
├── doctors/                  ← Doctor profiles, specializations
├── appointments/             ← Booking, prescriptions
├── pharmacy/                 ← Medicines, stock, dispensing
├── templates/                ← All HTML templates
│   ├── base/
│   ├── accounts/
│   ├── patients/
│   ├── doctors/
│   ├── appointments/
│   └── pharmacy/
├── static/                   ← CSS, JS, images
└── media/                    ← Uploaded files
```

---

## ⚡ Quick Start (Windows / macOS / Linux)

### 1. Create and Activate Virtual Environment

**Windows:**
```bash
python -m venv venv
venv\Scripts\activate
```

**macOS / Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Run Migrations
```bash
python manage.py makemigrations accounts patients doctors appointments pharmacy
python manage.py migrate
```

### 4. Populate Sample Data
```bash
python setup.py
```

### 5. Start Development Server
```bash
python manage.py runserver
```

### 6. Open in Browser
- **Home:**      http://127.0.0.1:8000/
- **Login:**     http://127.0.0.1:8000/accounts/login/
- **Admin:**     http://127.0.0.1:8000/admin/

---

## 🔑 Default Login Credentials

| Role  | Username | Password  |
|-------|----------|-----------|
| Admin | `admin`  | `admin123`|

> You can create additional users from the Register page.

---

## 🌟 Features

### 👤 Patient Management
- Add/Edit/Delete patient records
- Medical history with diagnosis, symptoms, treatment
- Vital signs tracking (BP, heart rate, temperature, BMI)
- Emergency contacts & insurance details
- Allergy and chronic condition tracking

### 🩺 Doctor Management
- Doctor profiles with specialization & qualifications
- Availability schedule (days & time)
- Consultation fee management
- Appointment history per doctor

### 📅 Appointment System
- Book appointments with date, time, type
- Status tracking: Scheduled → Confirmed → Completed
- Add prescriptions with multiple medicine items
- Follow-up date scheduling
- Today's schedule view

### 💊 Pharmacy Module
- Medicine inventory with stock levels
- Low stock & expiry alerts
- Dispense medicines with billing (₹)
- Stock movement history (in/out/adjustment)
- Category management

### 🔐 Authentication
- Role-based access (Admin, Doctor, Patient, Staff)
- User profiles with contact details
- Secure login/logout

---

## 🗃️ Database Models

| App          | Models                                          |
|--------------|-------------------------------------------------|
| accounts     | UserProfile                                     |
| patients     | Patient, MedicalRecord, VitalRecord             |
| doctors      | Doctor, Specialization                          |
| appointments | Appointment, Prescription, PrescriptionItem     |
| pharmacy     | Medicine, MedicineCategory, Dispensing, StockMovement |

---

## 🛠️ Tech Stack

- **Backend:** Django 4.2 (Python)
- **Database:** SQLite (development) — can switch to PostgreSQL
- **Frontend:** Bootstrap 5.3 + Font Awesome 6
- **Auth:** Django built-in authentication

---

## 🔧 Switching to PostgreSQL (Optional)

1. Install: `pip install psycopg2-binary`
2. Update `settings.py`:
```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'healthcare_db',
        'USER': 'your_user',
        'PASSWORD': 'your_password',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}
```

---

## 📸 Key Pages

| URL                          | Description              |
|------------------------------|--------------------------|
| `/`                          | Home / Landing Page      |
| `/dashboard/`                | Main Dashboard           |
| `/patients/`                 | Patient List             |
| `/patients/create/`          | Add New Patient          |
| `/doctors/`                  | Doctor List              |
| `/appointments/`             | All Appointments         |
| `/appointments/today/`       | Today's Schedule         |
| `/pharmacy/`                 | Pharmacy Dashboard       |
| `/pharmacy/medicines/`       | Medicine Inventory       |
| `/admin/`                    | Django Admin Panel       |

---

## 📝 License
MIT — Free to use for educational purposes.
