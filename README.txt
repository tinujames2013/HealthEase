# Hospital Management System

## Overview
This is a Hospital Management System that allows admins, doctors, and patients to manage hospital-related activities such as appointments, admissions, invoices, and more.

## Features

### Admin
- Signup/Login (No approval required)
- Manage doctors (approve/reject applications, delete doctors)
- Manage patients (admit, approve/reject, discharge patients)
- Generate and download invoices (based on treatment charges)
- Manage appointments (approve/reject patient requests)

### Doctor
- Apply for a job (admin approval required for login)
- View assigned patients and their details
- View discharged patients list
- Manage appointments (view/delete after attending)

### Patient
- Register/Login (admin approval required for login)
- View assigned doctor details
- Book and track appointment status (admin approval required)
- Download invoice (only after discharge)

## Contact Us Page Setup
- Configure email settings in `settings.py`:
  ```
  EMAIL_HOST_USER = 'youremail@gmail.com'
  EMAIL_HOST_PASSWORD = 'your email password'
  EMAIL_RECEIVING_USER = 'youremail@gmail.com'
  ```
- Enable access in Gmail settings.

## Important Notes
- Any user can register as an admin. To prevent this, disable admin signup and create a superuser manually.
- At least one doctor must be added before admitting patients.
- Ensure passwords are updated when modifying doctor/patient details.

## Setup Instructions
1. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
2. Apply migrations:
   ```sh
   python manage.py makemigrations
   python manage.py migrate
   ```
3. Create a superuser (for admin access):
   ```sh
   python manage.py createsuperuser
   ```
4. Run the server:
   ```sh
   python manage.py runserver
   ```

