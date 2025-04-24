# DPWH Fleet MS Project
# (SQL Server <> Power BI Integration)

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
git clone https://github.com/yourusername/DPWHFleetMS.git
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

### 3. Install Dependencies & Run the App

```bash
# Example for Node.js
npm install
npm start
```

Replace the commands above depending on your tech stack. For example:

- **Django**: `python manage.py runserver`  
- **.NET**: `dotnet run`

---

## 🔐 Database Connectivity Tips

To ensure proper SQL Server connectivity:

- ✅ Enable **TCP/IP** in SQL Server Configuration Manager  
- ✅ Set a **static port** (default is **1433**)  
- ✅ Use **SQL Server Authentication** (not just Windows Auth)  
- ✅ Open **port 1433** in your firewall if accessing remotely  

---

## 🛠️ Future Enhancements

- 🔍 Search by **DPCN** or **date range**  
- 📊 Dashboard of **equipment status trends**  
- 📤 Export to **Excel or PDF**  
- 👤 **User authentication and roles**  
- 📱 **Mobile-friendly interface**

---

## 📄 License

This project is licensed under the **MIT License**.

### ✅ What You Can Do:

- ✔️ Use the code for personal, academic, or commercial projects  
- ✔️ Modify the code to fit your needs  
- ✔️ Share, distribute, or even sell the software  

### 🚫 What You Can't Expect:

- ❌ The code comes with **no warranty**  
- ❌ The author is **not liable** for any damage or misuse  

### 📝 Conditions:

If you reuse or distribute this code:

- You must include the original **LICENSE** file  
- You must give **credit to the original author**
