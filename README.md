<div align="center">
<svg width="900" height="230" viewBox="0 0 900 230" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="bgG" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#FDF6EC"/>
      <stop offset="100%" stop-color="#FFFFFF"/>
    </linearGradient>
    <linearGradient id="blob1" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#FF7A5C"/>
      <stop offset="100%" stop-color="#FFB199"/>
    </linearGradient>
    <linearGradient id="blob2" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#2EC4B6"/>
      <stop offset="100%" stop-color="#8FE3D9"/>
    </linearGradient>
    <clipPath id="clip"><rect width="900" height="230" rx="16"/></clipPath>
  </defs>

  <!-- Background -->
  <rect width="900" height="230" fill="url(#bgG)" rx="16"/>
  <rect width="900" height="230" rx="16" fill="none" stroke="#EFE6D8" stroke-width="1.5"/>

  <g clip-path="url(#clip)">
    <!-- Soft decorative blobs -->
    <circle cx="40" cy="200" r="120" fill="url(#blob1)" opacity="0.14"/>
    <circle cx="860" cy="20" r="140" fill="url(#blob2)" opacity="0.14"/>
    <circle cx="850" cy="210" r="60" fill="#2EC4B6" opacity="0.08"/>

    <!-- Dotted accent pattern -->
    <g fill="#2EC4B6" opacity="0.25">
      <circle cx="40" cy="40" r="2.5"/><circle cx="60" cy="40" r="2.5"/><circle cx="80" cy="40" r="2.5"/>
      <circle cx="40" cy="58" r="2.5"/><circle cx="60" cy="58" r="2.5"/>
    </g>
    <g fill="#FF7A5C" opacity="0.25">
      <circle cx="820" cy="180" r="2.5"/><circle cx="840" cy="180" r="2.5"/>
      <circle cx="820" cy="198" r="2.5"/><circle cx="840" cy="198" r="2.5"/><circle cx="860" cy="198" r="2.5"/>
    </g>
  </g>

  <!-- Calendar icon card, left -->
  <g transform="translate(95,115)">
    <rect x="-32" y="-32" width="64" height="64" rx="16" fill="#FFFFFF" stroke="#FFD9CC" stroke-width="2"/>
    <rect x="-18" y="-14" width="36" height="28" rx="4" fill="none" stroke="#FF7A5C" stroke-width="3"/>
    <line x1="-18" y1="-6" x2="18" y2="-6" stroke="#FF7A5C" stroke-width="3"/>
    <line x1="-10" y1="-20" x2="-10" y2="-10" stroke="#FF7A5C" stroke-width="3" stroke-linecap="round"/>
    <line x1="10" y1="-20" x2="10" y2="-10" stroke="#FF7A5C" stroke-width="3" stroke-linecap="round"/>
    <circle cx="-7" cy="4" r="2.4" fill="#FF7A5C"/>
    <circle cx="4" cy="4" r="2.4" fill="#FF7A5C"/>
    <animateTransform attributeName="transform" type="translate" values="95,115;95,108;95,115" dur="3.5s" repeatCount="indefinite" additive="sum"/>
  </g>

  <!-- Heart/pulse icon card, right -->
  <g transform="translate(805,115)">
    <rect x="-32" y="-32" width="64" height="64" rx="16" fill="#FFFFFF" stroke="#BCEFE7" stroke-width="2"/>
    <path d="M-16,-2 C-16,-12 -2,-12 0,-2 C2,-12 16,-12 16,-2 C16,8 0,18 0,18 C0,18 -16,8 -16,-2 Z"
      fill="none" stroke="#2EC4B6" stroke-width="3" stroke-linejoin="round"/>
    <animateTransform attributeName="transform" type="translate" values="805,115;805,108;805,115" dur="3.5s" begin="1.2s" repeatCount="indefinite" additive="sum"/>
  </g>

  <!-- Eyebrow tag -->
  <g transform="translate(450,52)">
    <rect x="-92" y="-15" width="184" height="28" rx="14" fill="#2EC4B6" opacity="0.12"/>
    <text x="0" y="5" font-family="Arial, Helvetica, sans-serif" font-size="12" font-weight="700"
      text-anchor="middle" fill="#1B8A7E" letter-spacing="2">SMART CLINIC SYSTEM</text>
  </g>

  <!-- Main title -->
  <text x="450" y="118" font-family="Georgia, 'Times New Roman', serif" font-size="56" font-weight="700"
    text-anchor="middle" fill="#1F2A37">
    Clinic<tspan fill="#FF7A5C"> Flow</tspan>
  </text>

  <!-- Subtitle -->
  <text x="450" y="156" font-family="Arial, Helvetica, sans-serif" font-size="16"
    text-anchor="middle" fill="#6B7280">Your Health, Our Priority</text>

  <!-- Divider dots -->
  <g fill="#D1D5DB">
    <circle cx="390" cy="180" r="2"/>
    <circle cx="450" cy="180" r="2"/>
    <circle cx="510" cy="180" r="2"/>
  </g>

  <!-- Caption -->
  <text x="450" y="204" font-family="Arial, Helvetica, sans-serif" font-size="11"
    text-anchor="middle" fill="#9CA3AF" letter-spacing="1.5">
    Patients · Doctors · Admins — All in One Place
  </text>
</svg>

---
# 🏥 Clinic Flow

### *Your Health, Our Priority*![Uploading SHR4_SWD5_S1_PROJECT2_banner.svg…]()


A smart, all-in-one clinic management platform that brings patients, doctors, and administrators together in a single place.

<p>
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

<p>
  <a href="https://canva.link/gh7krkksr4u5bep"><img src="https://img.shields.io/badge/🎤_Presentation-FF6B6B?style=for-the-badge" alt="Presentation" /></a>
  <a href="https://drive.google.com/file/d/1csEcMRy4ylcjfsd7eTGx6p3zVzF4tSz6/view?usp=drive_link"><img src="https://img.shields.io/badge/📄_Documentation-4285F4?style=for-the-badge" alt="Documentation" /></a>
  <a href="https://drive.google.com/file/d/1zj_gs1uYiIjwUBXCNXQh0aqgoUQZgZsk/view?usp=drive_link"><img src="https://img.shields.io/badge/🎬_Demo_Video-34A853?style=for-the-badge" alt="Demo" /></a>
</p>

</div>

---

## 📌 Table of Contents

1. [About the Project](#-about-the-project)
2. [The Problem](#-the-problem)
3. [Our Solution](#-our-solution)
4. [Screenshots](#-screenshots)
5. [System Workflow](#-system-workflow)
6. [Architecture (N-Layer)](#-architecture-n-layer)
7. [Tech Stack](#-tech-stack)
8. [Security & Authentication](#-security--authentication)
9. [Modules](#-modules)
10. [Core Entities](#-core-entities)
11. [External Integrations](#-external-integrations)
12. [Key Features](#-key-features)
13. [Getting Started](#-getting-started)
14. [Resources](#-resources)
15. [Team](#-team)

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

## 📸 Screenshots

<div align="center">

<table>
  <tr>
    <td width="50%"><img src="https://github.com/user-attachments/assets/76042332-5fe9-4fec-8bbf-30f73a2fd137" alt="Clinic Flow screenshot 1" /></td>
    <td width="50%"><img src="https://github.com/user-attachments/assets/07bfab15-c491-424c-b13b-58eac224695a" alt="Clinic Flow screenshot 2" /></td>
  </tr>
  <tr>
    <td width="50%"><img src="https://github.com/user-attachments/assets/720f56a1-c9b0-4ebf-b989-6dea6817a037" alt="Clinic Flow screenshot 3" /></td>
    <td width="50%"><img src="https://github.com/user-attachments/assets/4b614d7e-f768-4727-b0e4-e902876164a4" alt="Clinic Flow screenshot 4" /></td>
  </tr>
  <tr>
    <td width="50%"><img src="https://github.com/user-attachments/assets/55b37fce-fb75-4084-bdb4-11f519d2dac8" alt="Clinic Flow screenshot 5" /></td>
    <td width="50%"><img src="https://github.com/user-attachments/assets/d826b94a-dfbf-4214-84d7-ebe2860bfbd4" alt="Clinic Flow screenshot 6" /></td>
  </tr>
  <tr>
    <td width="50%"><img src="https://github.com/user-attachments/assets/752e643c-e647-4cb2-95ae-f497a19d505e" alt="Clinic Flow screenshot 7" /></td>
    <td width="50%"><img src="https://github.com/user-attachments/assets/81a7e045-bf41-423b-a5e8-b2347b91a310" alt="Clinic Flow screenshot 8" /></td>
  </tr>
</table>

</div>

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

```
Clinic Flow
├── Clinic_System.DAL          → Data Access Layer
│   ├── Entities, Enums, Constants
│   ├── Data (DbContext) & Migrations
│   └── Repositories (IGenericRepository<T>, IUnitOfWork)
│
├── Clinic_System.BLL          → Business Logic Layer
│   ├── Services (IAppointmentService, IStripePaymentService, ...)
│   ├── DTOs
│   └── Helpers
│
└── custom_LogIn                → Presentation Layer
    ├── Controllers
    ├── Views (Razor)
    ├── ViewModels
    └── Templates (email templates)
```

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

## 🚀 Getting Started

### Prerequisites
- [.NET SDK](https://dotnet.microsoft.com/download) (8.0 or later)
- [SQL Server](https://www.microsoft.com/sql-server) (LocalDB or full instance)
- A [Stripe](https://stripe.com) account (test API keys)
- A Gmail account with an App Password for SMTP

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/ItcProjects-R4/SHR4_SWD5_S1_PROJECT4.git

# 2. Navigate to the project folder
cd SHR4_SWD5_S1_PROJECT4

# 3. Restore packages
dotnet restore

# 4. Set up the database (update the connection string in appsettings.json)
dotnet ef database update --project Clinic_System.DAL

# 5. Configure Stripe and Gmail SMTP credentials (API keys) in appsettings.json

# 6. Run the project
dotnet run --project custom_LogIn
```

The app will be available at `https://localhost:{port}` once it starts.

---

## 📚 Resources

| Resource | Link |
|---|---|
| 🎤 Presentation | [View on Canva](https://canva.link/gh7krkksr4u5bep) |
| 📄 Documentation | [View on Google Drive](https://drive.google.com/file/d/1csEcMRy4ylcjfsd7eTGx6p3zVzF4tSz6/view?usp=drive_link) |
| 🎬 Demo Video | [View on Google Drive](https://drive.google.com/file/d/1zj_gs1uYiIjwUBXCNXQh0aqgoUQZgZsk/view?usp=drive_link) |

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

<div align="center">

**ITC Colleague — Ministry of Communications and Information Technology | Egypt's Digital Pioneers Initiative**

</div>
