# Project Overview

## Goal

The Clinic Management System is a web application designed to organize common clinic workflows in one place: patient records, medical scheduling, visits, billing, and internal communication.

The project was built as a practical ASP.NET Core learning project with an emphasis on well-structured CRUD operations and relational data management.

## Solution Structure

```text
ClinicManagementSystem
├── Web
│   ├── Controllers
│   ├── Views
│   ├── ViewModels
│   └── wwwroot
├── Application-Bll
│   ├── DTOs
│   ├── Interfaces
│   ├── Services
│   ├── Validators
│   └── MappingProfile.cs
├── Domain.Bll
│   ├── Entities
│   └── Enums
└── Infrastructure.DAL
    ├── Data
    ├── Configurations
    └── Migrations
```

## Layer Responsibilities

| Layer | Responsibility |
|---|---|
| Web | ASP.NET Core MVC controllers, Razor views, form handling, and the user interface |
| Application-Bll | Application services, DTOs, mappings, validation, and use-case coordination |
| Domain.Bll | Core entities, enums, and business concepts |
| Infrastructure.DAL | Entity Framework Core data access, SQL Server mappings, and migrations |

## Key Workflows

### Patient lifecycle

1. Register a patient and generate/store their medical details.
2. Search and review the patient profile.
3. Schedule an appointment with a doctor.
4. Record the visit and related medical notes.
5. Create the invoice and register one or more payments.

### Scheduling

Appointments connect patients and doctors with a date/time, room, notes, and a status. Visits may link back to their originating appointment, which preserves the flow from booking to consultation.

### Billing

Invoices are associated with visits and hold totals, discount information, patient share, insurance share, and payment status. Payments are recorded with date and method such as cash, card, insurance, or bank transfer.

## Data Relationships

- A department can contain multiple doctors.
- A patient can have multiple appointments and visits.
- A doctor can manage multiple appointments and visits.
- A visit may optionally originate from an appointment.
- A visit can have an invoice.
- An invoice can have one or more payments.

## Why This Project Matters

This project demonstrates hands-on work with:

- ASP.NET Core MVC request/response flow
- C# object-oriented design
- Entity Framework Core relationships and configurations
- SQL Server persistence
- Service and repository-style separation of concerns
- Form validation and error handling
- UI integration for real-world data-management screens

## Privacy and Availability

The source project is private. This public portfolio intentionally excludes source code, connection strings, local configuration, internal documentation, and any data that could identify patients or users.
