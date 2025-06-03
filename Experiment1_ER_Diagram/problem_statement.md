# Experiment 1: Entity-Relationship (ER) Diagram

#### Name: Oswald Shilo  
#### Registration No: 212223040139  

---

## 🎯 Objective
To understand and apply the concepts of ER modeling by creating an ER diagram for a real-world application.

---

## 📚 Purpose
The purpose of this workshop is to gain hands-on experience in designing ER diagrams that visually represent the structure of a database including entities, relationships, attributes, and constraints.

---

## 🧪 Scenario Chosen
**Scenario: Hospital Database**

---

## 🗂️ ER Diagram
![Hospital ER](https://github.com/user-attachments/assets/5890c2bb-9551-497d-8ddd-759dad4110d9)

---

## 🧱 Entities and Attributes

- **Department of Specialization**
  - Department ID
  - Department Name
  - Head of Department

- **Doctor**
  - First Name
  - Last Name
  - Specialization
  - Email
  - Phone No.

- **Patient**
  - Patient ID
  - Full Name
  - Email
  - Phone No.

- **Appointments**
  - Appointment ID
  - Patient Name
  - Doctor Name
  - Date
  - Time

- **Medical Records**
  - Medical Record ID
  - Patient Name
  - Doctor Name
  - Diagnosis
  - Medication

---

## 🔗 Relationships and Constraints

- **`consists of`**
  - Entities: Department of Specialization — Doctor  
  - Cardinality: One Department → Many Doctors (1:N)  
  - Participation: Total on Doctor

- **`treats`**
  - Entities: Doctor — Patient  
  - Cardinality: One Doctor → Many Patients (1:N)  
  - Participation: Total on Patient

- **`schedules`**
  - Entities: Patient — Appointments  
  - Cardinality: One Patient → Many Appointments (1:N)  
  - Participation: Partial on Appointment

- **`collects`**
  - Entities: Appointments — Medical Records  
  - Cardinality: One Appointment → One Medical Record (1:1)  
  - Participation: Total on Medical Record

---

## 💳 Extension: Billing (Optional)

In this design, the billing aspect is assumed to occur **after each appointment**, based on the services rendered. While not explicitly modeled in the ER diagram provided, this could be extended using an additional `Billing` entity linked to `Appointments`, capturing:

- Billing ID
- Appointment ID (FK)
- Amount
- Payment Method
- Payment Date

---

## 📐 Design Choices

### ➤ Entities:
- **Department of Specialization**: Organizes doctors based on their specialties, aiding administrative structure.
- **Doctor**: Represents medical professionals with their qualifications and contact information.
- **Patient**: Central to the system, capturing their personal and contact details.
- **Appointments**: Connects patients and doctors at specific times for tracking interactions.
- **Medical Records**: Documents diagnoses and treatments for patient history and continuity of care.

### ➤ Relationships:
- **Department → Doctor (1:N)**: Each doctor belongs to a department; one department can have many doctors.
- **Doctor → Patient (1:N)**: A doctor may treat many patients.
- **Patient → Appointments (1:N)**: A patient can schedule multiple appointments.
- **Appointments → Medical Records (1:1)**: Each appointment results in exactly one medical record.

---

## 🧠 Assumptions

- **Single Specialization per Doctor**: Each doctor has one primary specialization.
- **One Medical Record per Appointment**: Each appointment corresponds to one unique medical record.
- **Doctor Assignment is Static per Appointment**: Each appointment is between one patient and one doctor.
- **Billing is Event-Based**: Billing occurs post-appointment and reflects services provided during that session.

---

## ✅ RESULT
Hence, the concepts of ER modeling were understood and applied effectively by creating an ER diagram for a real-world hospital application.
