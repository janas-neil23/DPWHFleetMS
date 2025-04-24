# DPWH Fleet MS Project (SQL Server <> Power BI Integration)

This repository contains the development resources for a Fleet Management System that leverages SQL Server for data warehousing and Power BI for business intelligence and data visualization.

---

## 📌 Overview

This project helps users:
- **Register equipment** by DPCN and issuance date
- **Log daily status** for each equipment item
- **View and manage historical data** on equipment condition

It’s built with a simple schema to prioritize usability and speed — and designed to grow with your needs.

---

## ✨ Features

- ✅ Register new equipment  
- 🕓 Log equipment status updates with date and time  
- 🗂️ View and edit historical records  
- 🗑️ Delete records when necessary  

---

## 🗃️ Data Model

| Field              | Type               | Description                      |
|-------------------|--------------------|----------------------------------|
| **DPCN**           | `VARCHAR` / `NVARCHAR` | Unique identifier of the equipment |
| **Issuance Date**  | `DATE`             | Date the equipment was issued    |
| **Date Log**       | `DATETIME`         | Timestamp for the status log     |
| **Equipment Status** | `VARCHAR`        | Description of current status    |

---

## 🖥️ Tech Stack

- **Frontend**: HTML/CSS + JavaScript (or React if preferred)  
- **Backend**: .NET / Node.js / Python Flask/Django (your choice)  
- **Database**: **Microsoft SQL Server**

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/equipment-status-logger.git
cd equipment-status-logger
```

### 2. Set Up SQL Server

- Ensure SQL Server is running  
- Create the database and table using the SQL script below  
- Update your database connection string in your app’s config file (e.g. `.env`, `settings.py`, or `app.config`)

```sql
CREATE TABLE EquipmentStatus (
    ID INT PRIMARY KEY IDENTITY(1,1),
    DPCN NVARCHAR(50) NOT NULL,
    IssuanceDate DATE NOT NULL,
    DateLog DATETIME NOT NULL,
    EquipmentStatus NVARCHAR(255) NOT NULL
);
```

## 3. Install Dependencies & Run the App

```bash
# Example for Node.js
npm install
npm start
```
