Hospital_management_system
ER diagram and MySQL table conversion using XAMPP

Team members:
Vaibhavi Mishra — 2410030131
Abhishek Kumar Sharma — 2410030395
Devashish Yadav — 2410030125
Shreya Srivastava — 2410030334

Description
This project contains an ER diagram and MySQL table conversion for a Hospital Management System.

Contents
ER Diagram (PDF)
MySQL SQL file for XAMPP (phpMyAdmin)
Tools Used
MySQL
XAMPP
How to Run
Open XAMPP and start Apache & MySQL
Open phpMyAdmin
Create database: hospital_management
Import the SQL file from Database folder
Entities and Attributes Used
1. Department
dept_id (Primary Key)
dept_name
HOD
location (building, floor, room_no)
phone_no (multivalued)
2. Doctor
doctor_id (Primary Key)
Name-
f_name
m_name
l_name
specialisation
experience
dept_id (Foreign Key)
phone_no (multivalued)
3. Patient
patient_id (Primary Key)
Name-
f_name
m_name
l_name
age
gender
phone_no (multivalued)
4. Appointment
apt_id (Primary Key)
apt_date
apt_time
doctor_id (Foreign Key)
patient_id (Foreign Key)
5. Prescription
presc_id (Primary Key)
issued_date
doctor_id (Foreign Key)
patient_id (Foreign Key)
apt_id (Foreign Key)
medicine (multivalued)
Relationships and Cardinality
Department – Doctor One department can have many doctors (1 : N)

Doctor – Appointment One doctor can conduct many appointments (1 : N)

Patient – Appointment One patient can book many appointments (1 : N)

Doctor – Prescription One doctor can issue many prescriptions (1 : N)

Patient – Prescription One patient can receive many prescriptions (1 : N)

Prescription – Medicine One prescription can contain many medicines (1 : N, multivalued attribute)

Tables Created in Database
department
department_contact
doctor
doctor_contact
patient
patient_phone
appointment
prescription
prescription_medicine
