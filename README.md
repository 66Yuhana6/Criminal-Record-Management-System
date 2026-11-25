# Criminal Management System

A **5th-semester academic project** built with **Core PHP** and **MySQL** to digitize and manage criminal records, case registrations, court details, prison records, and crime classifications using full **CRUD (Create, Read, Update, Delete)** operations.

---

## System Architecture & Workflow Chart

```mermaid
flowchart TD
    A[Admin Login Portal] -->|Authenticated| B[Admin Dashboard]
    B --> C[Administration Modules]
    B --> D[Reports & Search]
    B --> E[Change Password]

    C --> C1[Add Criminal]
    C --> C2[Add Crime]
    C --> C3[Add Court]
    C --> C4[Add Prison]
    C --> C5[Add Crime Category]

    C1 & C2 & C3 & C4 & C5 --> F[(MySQL Database: db_criminal_record)]
    F --> D
    D --> D1[Crime Reports - Edit / Delete]
    D --> D2[Criminal Reports & Profile Cards]
    D --> D3[Court & Prison Reports]
    D --> D4[Crime Category Reports]
```

---

## Key Features & CRUD Modules

| Module | Operations Supported | Description |
| :--- | :--- | :--- |
| **Admin Authentication** | Login, Password Update | Secures administrative access (`admin/`) with session validation and password management. |
| **Criminal Management** | Create, Read, Update, Delete | Registers criminal profiles with photo uploads, contact details, date of birth, address, and biometric metrics (height & weight). |
| **Crime Registration** | Create, Read, Update, Delete | Links registered criminals to specific crime categories, prisons, courts, dates, locations, and case descriptions. |
| **Court Management** | Create, Read, Update, Delete | Maintains court records including court name, court type, location, and description. |
| **Prison Management** | Create, Read, Update, Delete | Tracks correctional facilities, locations, and facility details. |
| **Crime Category Management** | Create, Read, Update, Delete | Organizes offense classifications and descriptions across the system. |
| **Reports & Search** | Read, Filter, Edit, Delete | Displays structured tables and profile cards with quick search filtering and instant action controls. |

---

## Database Schema (`db_criminal_record`)

| Table Name | Purpose |
| :--- | :--- |
| `tbl_admin` | Stores administrator credentials and login details. |
| `tbl_criminal` | Stores personal details, biometrics, contact info, and photo paths of registered criminals. |
| `tbl_crime` | Stores registered crime incidents linked to criminal, category, prison, and court IDs. |
| `tbl_crime_category` | Stores master crime types and descriptions. |
| `tbl_court` | Stores master court names, types, and locations. |
| `tbl_prison` | Stores master prison names, locations, and descriptions. |

---

## Tech Stack

| Layer | Technology |
| :--- | :--- |
| **Backend** | Core PHP |
| **Database** | MySQL (`phpMyAdmin`) |
| **Frontend** | HTML5, CSS3, JavaScript, Bootstrap |
| **Local Server** | XAMPP (Apache & MySQL) |

---

## Project Screenshots

| Crime Registration Form | Crime Reports |
| :---: | :---: |
| ![Crime Registration](screenshots/crime-registration.png) | ![Crime Reports](<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c6ae0555-79d9-42a8-a8c8-cc86dac67238" />
) |

| Criminal Reports Table | Criminal Profile Cards & Search |
| :---: | :---: |
| ![Criminal Reports](screenshots/criminal-reports.png) | ![Criminal Profiles](screenshots/criminal-profiles.png) |

| Court Reports | Prison Reports |
| :---: | :---: |
| ![Court Reports](screenshots/court-reports.png) | ![Prison Reports](screenshots/prison-reports.png) |

| Crime Category Reports |
| :---: |
| ![Category Reports](screenshots/category-reports.png) |

---

## Local Setup & Installation

1. **Install XAMPP:** Download and install XAMPP on your system, then start **Apache** and **MySQL** from the XAMPP Control Panel.
2. **Place Project Files:** Copy this repository into your `htdocs` folder:
   ```text
   C:\xampp\htdocs\crms\Criminal_Management_System
   ```
3. **Create Database:** Open `http://localhost/phpmyadmin`, click **New**, and create a database named:
   ```text
   db_criminal_record
   ```
4. **Import SQL File:** Select `db_criminal_record`, open the **Import** tab, choose `database/db_criminal_record.sql`, and click **Import**.
5. **Run the Application:** Open your browser and visit:
   ```text
   http://localhost/crms/Criminal_Management_System/admin/
   ```
