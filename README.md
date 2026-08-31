# Clinic Management System — Portfolio

A portfolio overview of a **Clinic Management System** built with ASP.NET Core.  
This repository is intentionally documentation-only: the production/source repository remains private while this page presents the project scope and the work implemented.

> Focus: clean, maintainable CRUD workflows for clinic operations.

## What I Built

The project supports the core day-to-day flow of a clinic:

- Patient registration and profile management
- Doctors and departments management
- Appointment scheduling and status tracking
- Visits and medical records
- Invoice and payment management
- User accounts, roles, messages, and notifications

The work focused mainly on designing and implementing reliable **Create, Read, Update, and Delete (CRUD)** operations with validation, related data handling, and a consistent MVC user experience.

## Technical Stack

| Area | Technologies |
|---|---|
| Backend | C#, ASP.NET Core MVC |
| Data access | Entity Framework Core, LINQ |
| Database | SQL Server |
| Architecture | Clean Architecture-inspired layered solution |
| Mapping & validation | AutoMapper, FluentValidation |
| Front end | Razor Views, Bootstrap, JavaScript/jQuery |
| UI components | DataTables, Select2, SweetAlert2, Chart.js, FullCalendar |
| Source control | Git & GitHub |

## Architecture

```text
Web (ASP.NET Core MVC)
        ↓
Application (DTOs, services, validation, mappings)
        ↓
Domain (entities, enums, business models)
        ↓
Infrastructure (EF Core, DbContext, configurations, SQL Server)
```

Keeping business rules and persistence outside the MVC layer makes the codebase easier to test, change, and extend.

## Main Modules

| Module | Examples of implemented CRUD work |
|---|---|
| Patients | Create patient records, search/list, edit demographic details, view history |
| Doctors & departments | Manage doctor profiles and department assignment |
| Appointments | Create and manage appointment dates, rooms, notes, and statuses |
| Visits & records | Record clinic visits and link medical information to the patient |
| Billing | Create invoices, apply discounts, register payments, track status |
| Users & communication | Manage users/roles and support messages and notifications |

## Selected Domain Model

- **Patient** — medical record number, contact details, insurance data
- **Doctor** — specialty, department, availability data
- **Appointment** — patient, doctor, date/time, room, status
- **Visit** — optional appointment, department, visit status and notes
- **Invoice / Payment** — totals, discounts, payment method and status
- **User / Message / Notification** — role-based accounts and internal communication

## Engineering Notes

- Entity Framework Core configurations define entity relationships and protect data consistency.
- DTOs separate web-facing input/output from domain entities.
- Validation is applied to important forms such as patients, doctors, appointments, and invoices.
- Shared layouts and reusable UI components keep the MVC interface consistent.
- The project was developed as a practical learning project to strengthen ASP.NET Core, C#, SQL, and CRUD design skills.

## About Me

I am **Ragab Adel**, a Junior .NET Developer transitioning from an IT Support background into backend and full-stack development.

I am looking for Junior / Entry-Level opportunities in:

- ASP.NET Core / .NET Backend Development
- C# and SQL Server development
- MVC and Web API applications

[View my GitHub profile](https://github.com/ragabadel)

---

*This portfolio documents the project architecture and implemented functionality without publishing private source code, configuration, or client data.*
