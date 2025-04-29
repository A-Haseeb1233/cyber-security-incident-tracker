# cyber-security-incident-tracker
Author - Abdul Haseeb
# 🛡️ Cybersecurity Incident Tracker

A relational database project designed to log, manage, and analyze cybersecurity incidents across departments and locations. Developed using SQL and deployed via Neon.tech, this schema models real-world incident handling in organizations.

---

## ⚙️ Technologies Used

| Tool/Technology     | Purpose                                    |
|---------------------|--------------------------------------------|
| **SQL (T-SQL / PostgreSQL)** | For designing and querying the database       |
| **Neon.tech**        | Cloud-based Postgres database hosting     |
| **Git & GitHub**     | Version control and repository management |
| **GitHub Codespaces**| Cloud IDE for remote SQL development      |
| **Markdown**         | For documentation and project README      |

---

## 🗂️ Database Schema Overview

The database consists of the following main entities:

- **Departments** – Tracks organizational units  
- **Locations** – Represents physical or virtual locations  
- **Users** – Employees/users who report or handle incidents  
- **Systems** – Assets or infrastructure where incidents occur  
- **IncidentTypes** – Categories like phishing, malware, etc.  
- **SeverityLevels** – Impact levels (Low, Medium, High)  
- **IncidentStatus** – Tracks status (Open, In Progress, Closed)  
- **Incidents** – Central incident logging table  
- **IncidentActions** – Actions taken to resolve incidents  

---

## 🧱 Schema Diagram (Text Summary)

```plaintext
Departments <── Users ──> Locations
        │                   │
        └──── Systems ─────┘

IncidentTypes ─┐
SeverityLevels ├──> Incidents <── Users (ReportedBy)
IncidentStatus ┘                 │
                                 └─> IncidentActions <── Users (TakenBy)
