# 🏥 Clinic Flow

> **Your Health, Our Priority**

A smart, all-in-one clinic management platform that brings patients, doctors, and administrators together in a single place.

<p align="left">
  <img src="https://img.shields.io/badge/.NET-512BD4?style=for-the-badge&logo=dotnet&logoColor=white" alt=".NET" />
  <img src="https://img.shields.io/badge/ASP.NET%20Core-512BD4?style=for-the-badge&logo=dotnet&logoColor=white" alt="ASP.NET Core" />
  <img src="https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=csharp&logoColor=white" alt="C#" />
  <img src="https://img.shields.io/badge/Entity%20Framework%20Core-512BD4?style=for-the-badge&logo=dotnet&logoColor=white" alt="EF Core" />
  <img src="https://img.shields.io/badge/SQL%20Server-CC2927?style=for-the-badge&logo=microsoftsqlserver&logoColor=white" alt="SQL Server" />
  <img src="https://img.shields.io/badge/Stripe-008CDD?style=for-the-badge&logo=stripe&logoColor=white" alt="Stripe" />
  <img src="https://img.shields.io/badge/Razor%20Pages-512BD4?style=for-the-badge&logo=dotnet&logoColor=white" alt="Razor" />
  <img src="https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white" alt="Tailwind CSS" />
  <img src="https://img.shields.io/badge/DaisyUI-5A0EF8?style=for-the-badge&logo=daisyui&logoColor=white" alt="DaisyUI" />
  <img src="https://img.shields.io/badge/Google%20OAuth-4285F4?style=for-the-badge&logo=google&logoColor=white" alt="Google OAuth" />
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git" />
</p>

---

## 📌 Table of Contents

1. [About the Project](#-about-the-project)
2. [The Problem](#-the-problem)
3. [Our Solution](#-our-solution)
4. [System Workflow](#-system-workflow)
5. [Architecture (N-Layer)](#-architecture-n-layer)
6. [Tech Stack](#-tech-stack)
7. [Security & Authentication](#-security--authentication)
8. [Modules](#-modules)
9. [Core Entities](#-core-entities)
10. [External Integrations](#-external-integrations)
11. [Key Features](#-key-features)
12. [Screenshots](#-screenshots)
13. [Getting Started](#-getting-started)
14. [Team](#-team)

---

## 💡 About the Project

**Clinic Flow** is a complete electronic clinic management system. Patients can register, browse departments and doctors, book and pay for appointments online, and cancel with ease — while administrators get full visibility into everything happening in the clinic: appointments, requests, and refunds, all in one dashboard.

---

## ⚠️ The Problem

Most clinics still rely on phone calls to find the right department, doctor, or available time slot. This leaves patients with no real-time view of actual open appointments, which often leads to double-booking and forces staff to resolve conflicts manually. Cancellations and refunds are tracked on paper or scattered spreadsheets, and patients frequently forget appointments due to the lack of automated reminders. The result: frustrated patients, overworked front-desk staff, and a clinic with no clear view of its own schedule.

---

## 🩺 Our Solution

Clinic Flow brings patients and clinic staff onto one unified platform:

- **Patients** can create an account, browse departments and doctors, book and pay for appointments, and cancel online.
- **Admins** get a complete view of everything happening in the clinic — appointments, requests, and refunds — in one place.

---

## 🔄 System Workflow

**New Patient Registration & Appointment Booking Flow:**

1. **Patient Registration** — New visitors create an account with name, email, and password.
2. **Doctor Selection** — Patients browse doctor profiles and choose the right specialty.
3. **Department Browsing** — Registered patients explore available medical departments.
4. **Time Slot Selection** — Choose a convenient date and time for the appointment.
5. **Appointment Confirmation** — Patients review and confirm the selected appointment.
6. **Payment** — Complete payment through multiple methods via Stripe.
7. **Booking Confirmation** — Receive an instant confirmation and appointment reminders.
8. **View Appointments** — Track current and past appointments.
9. **Edit Personal Information** — Update profile details.
10. **Cancel Appointment** — Cancel an appointment, optionally with a reason.
11. **Search** — Search for a doctor or clinic.
12. **Logout** — Secure sign-out.
13. **Contact Form** — Reach support with any inquiry.

---

## 🏗️ Architecture (N-Layer)

The project is divided into **three fully independent layers**, each with a single responsibility (Separation of Concerns):

### 🗄️ Data Access Layer (DAL)
- Responsible solely for interacting with the database.
- Contains: Entities, Enums, Constants, Data (DbContext), Migrations, and Repositories.
- Implements the **Repository Pattern** via `IGenericRepository<T>` and the **Unit of Work Pattern** via `IUnitOfWork` — every database operation passes through a single unified intermediary layer, so no Controller or Service talks to the database directly.

### ⚙️ Business Logic Layer (BLL)
- Contains all business logic, fully decoupled from both the database and the UI.
- Implements the **Service Layer Pattern**: every operation (booking an appointment, processing a payment, registering a doctor...) has its own Interface + Service (e.g. `IAppointmentService` / `AppointmentService`).
- Also includes **DTOs** (Data Transfer Objects) so raw Entities are never exposed directly to the presentation layer, plus Helpers for supporting logic.

### 🖥️ Presentation Layer (PL) — named `custom_LogIn` in the project
- Contains Controllers, Views (Razor), ViewModels, and Templates (email templates).
- The only layer that interacts directly with the user (HTTP Requests/Responses).

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| **ASP.NET Core (.NET)** | Core application framework |
| **Entity Framework Core** | ORM for database access |
| **SQL Server** | Database |
| **Repository + Unit of Work Pattern** | Data access management |
| **Service Layer Pattern** | Business logic organization |
| **ASP.NET Core Identity** | User and role management |
| **Stripe.net** | Online payment processing |
| **MailKit + MimeKit** | Email delivery via SMTP |
| **Razor Views** | Presentation layer UI |
| **Tailwind CSS & DaisyUI** | Frontend styling |
| **Google OAuth 2.0** | Sign-in with Google |

---

## 🔐 Security & Authentication

One of the strongest technical aspects of the project:

- **ASP.NET Core Identity** (`AddIdentityCore<User>`) for user management, with **Roles** (`AddRoles<IdentityRole>`) to distinguish between Admin / Doctor / Patient.
- **Cookie Authentication** as the core auth mechanism, including:
  - **Sliding Expiration** — the cookie automatically refreshes with use, with a 7-day lifespan.
  - **Security Stamp Validation** — every request is checked against the database's security stamp; if the password changes, the user is immediately logged out everywhere.
- **Google OAuth 2.0** (`AddGoogle`) — sign-in with Google using a separate temporary cookie (`ExternalCookie`) dedicated to the external login flow, so it never conflicts with the main session cookie.
- **Password Policy**: minimum 8 characters, with email confirmation required before login.

---

## 📦 Modules

### 👤 Patient Module
- Dashboard showing total, upcoming, and completed appointments
- Personal profile management (name, date of birth, email, medical history)
- Detailed appointment tracking (doctor, date, status, fees, payment status)

### 🩺 Doctor Module
- Dashboard showing appointment count, patients, revenue, and rating
- Appointment status tracking (Pending / Confirmed / Completed / Cancelled)
- Professional profile management (specialty, years of experience, consultation fees, bio)
- View latest patient reviews

### 🛡️ Admin Module
- Comprehensive dashboard: patient count, doctor count, appointments, and monthly revenue
- Track the status of every appointment in the clinic
- View top-performing doctors and the latest payments
- Manage administrative profile data

### 💳 Booking & Payment Module
- Appointment booking page per doctor, showing price, specialty, and rating
- Secure online payment via **Stripe** with multiple payment methods
- Instant booking confirmation after payment

---

## 🧩 Core Entities

`User`, `Patient`, `Doctor`, `Department`, `Specialty`, `Schedule`, `Appointment`, `Payment`, `Review`, `CancellationRequest`, `Address`, `Contact`, `SmartClinic`

Every entity inherits from `BaseEntity` to share common properties such as `Id` and creation timestamps.

---

## 🔌 External Integrations

| Service | Description |
|---|---|
| **Stripe (Stripe.net)** | A complete global payment system, handled through `IStripePaymentService` / `StripePaymentService` and a dedicated `PaymentController` for appointment payments |
| **MailKit + MimeKit (SMTP)** | Email delivery via SMTP (configured with a Gmail account), with ready-made HTML templates (e.g. `ConfirmEmail.html`) loaded and populated dynamically via `IEmailTemplateService` |
| **Google OAuth 2.0** | Sign-in with Google as an alternative authentication method |

---

## 💎 Key Features

- ✅ Clean, scalable N-Layer architecture (DAL / BLL / PL)
- ✅ Repository + Unit of Work Pattern for unified data management
- ✅ Service Layer Pattern with DTOs to shield Entities from direct exposure
- ✅ Multi-role permission system (Admin / Doctor / Patient)
- ✅ Secure authentication with Cookie + Security Stamp Validation + Google Sign-In
- ✅ Secure online payments via Stripe
- ✅ Automated email notifications and reminders
- ✅ Doctor and clinic search with filtering by specialty and price
- ✅ Full management of cancellation and refund requests

---

## 📸 Screenshots

> *(Taken from the project presentation)*

- Home page: "Your Health, Our Priority"
- Login page with "Continue with Google" option
- Medical departments page (Cardiology, Dermatology, Neurology, Orthopedics, Pediatrics, Dentistry, ENT, Ophthalmology)
- "Meet Our Specialists" page with search filters (doctor name, specialty, max price)
- Per-doctor booking and payment page
- Patient / Doctor / Admin dashboards

> *[Add actual screenshots here if available]*

---

## 🚀 Getting Started

```bash
# 1. Clone the repository
git clone [repo-url]

# 2. Navigate to the project folder
cd Clinic_Flow

# 3. Restore packages
dotnet restore

# 4. Set up the database (update the connection string in appsettings.json)
dotnet ef database update --project Clinic_System.DAL

# 5. Configure Stripe and Gmail SMTP credentials (API keys) in appsettings.json

# 6. Run the project
dotnet run --project custom_LogIn
```

> *[Add any additional setup instructions here]*

---

## 👥 Team

**Team Members:**

| Name | Role |
|---|---|
| Ahmed Hosny | Team Leader |
| Sama Mohamed Khalafallah | Team Member |
| Mennatullah Ahmed Mohamed | Team Member |
| Ibrahim Karam Atia | Team Member |

**Under Supervision:**

- Dr. Mahmoud Raslan
- Eng. Ibrahim Abdelhamid

**ITC Colleague — Ministry of Communications and Information Technology | Egypt's Digital Pioneers Initiative**
