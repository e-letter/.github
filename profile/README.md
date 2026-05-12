# E-Letter Organization 📝

> **Complete school permission letter management system** across web, desktop, and mobile platforms with modern interfaces, seamless user experience, and comprehensive letter tracking.

[![Website](https://img.shields.io/badge/Web-Next.js%2016-000?logo=next.js)](https://github.com/e-letter/e-letter-web)
[![Desktop](https://img.shields.io/badge/Desktop-.NET%204.7.2-512BD4?logo=dot-net)](https://github.com/e-letter/e-letter-desktop)
[![Mobile](https://img.shields.io/badge/Mobile-Android%2014-3DDC84?logo=android)](https://github.com/e-letter/e-letter-android)
[![License](https://img.shields.io/badge/License-Proprietary-red)](LICENSE)

---

## 📊 Platform Overview

| Platform   | Framework                 | Language   | Key Features                                           | Repository                                                       |
| ---------- | ------------------------- | ---------- | ------------------------------------------------------ | ---------------------------------------------------------------- |
| 🌐 Web     | Next.js 16 + Tailwind CSS | TypeScript | Real-time tracking, Multi-stage approval, Beautiful UI | [e-letter-web](https://github.com/e-letter/e-letter-web)         |
| 🖥️ Desktop | .NET 4.7.2 + WPF          | C#         | Offline support, Local storage, Native Windows         | [e-letter-desktop](https://github.com/e-letter/e-letter-desktop) |
| 📱 Mobile  | Android 14+ / Kotlin      | Kotlin     | Mobile-optimized, Push notifications, Biometric auth   | [e-letter-android](https://github.com/e-letter/e-letter-android) |

---

## 🎯 About E-Letter

E-Letter is a comprehensive **school permission letter management system** designed to streamline managing student permission requests across multiple platforms. Built with a dual-backend architecture (Go API + Next.js frontend) and native platform clients, it delivers a consistent experience across Web, Desktop, and Mobile.

### Core Capabilities

- **Multi-Platform Access** - Web, Desktop, and Mobile with unified workflows
- **Role-Based Access Control** - Students, Teachers, Principals, and Administrators with tailored dashboards
- **Real-Time Tracking** - Live status updates on permission requests (web & mobile)
- **Multi-Stage Approval Workflow** - Complete letter routing with digital signatures
- **Secure Authentication** - JWT tokens (web), session-based (desktop/mobile)
- **Beautiful Modern UI** - Consistent gradient design system across all platforms
- **Complete Audit Trail** - Comprehensive history and logging of all actions

### Permission Types

| Type         | Code | Color     | Description                        | Use Case                       |
| ------------ | ---- | --------- | ---------------------------------- | ------------------------------ |
| Entry        | IM   | 🔵 Purple | Late arrival or post-absence entry | Student arrives late to school |
| Exit         | IK   | 🟠 Orange | Early departure permission         | Student needs to leave early   |
| Dispensation | DISP | 🟡 Yellow | Special exemptions/exclusions      | Medical/family emergencies     |

---

## 🌐 Web Application

A modern, interactive web application for managing school permission letters with beautiful UI and seamless user experience. Built with Next.js 16 App Router, TypeScript, and a Go-powered backend API.

### Web Features

- **Gradient Design System** - Custom purple, orange, yellow, and blue themes with glassmorphism
- **Smooth Animations** - Framer Motion powered transitions and micro-interactions
- **Responsive Design** - Fully responsive across all devices
- **Role-Based Dashboards** - Student Portal, Teacher Dashboard, Admin Panel
- **Real-Time Status Tracking** - Live approval progress updates
- **Multi-Stage Approval** - Complete workflow with audit trails
- **Digital Signatures** - Canvas-based signature capture
- **JWT Authentication** - Secure token-based with refresh tokens
- **Docker Ready** - One-command deployment

### Web Tech Stack

| Component      | Technology                     |
| -------------- | ------------------------------ |
| **Framework**  | Next.js 16 (App Router)        |
| **Language**   | TypeScript 5.0                 |
| **Styling**    | Tailwind CSS 4 + Framer Motion |
| **UI Library** | shadcn/ui components           |
| **Database**   | MariaDB 11.5                   |
| **Backend**    | Go 1.22 + Gin framework        |
| **Auth**       | JWT with access/refresh tokens |
| **Deploy**     | Docker & Docker Compose        |

### Web Quick Start

```bash
git clone https://github.com/e-letter/e-letter-web.git
cd e-letter-web
bun install
cp .env.example .env.local
docker-compose up -d
bun dev
```

### Web Database Architecture

The web database uses **5 logical sections**:

1. **Reference Tables** - Roles, majors, classes, permission types
2. **User Management** - Users, profiles, authentication tokens
3. **Permission System** - Requests, approval stages, approval logs
4. **Supporting Data** - Dispensations, attachments, letter sequences
5. **Audit & Logging** - Login logs, system audit trails

Key tables: `users`, `permission_requests`, `approval_stages`, `permission_approval_logs`, `dispensation_students`

👉 [View Web Project](https://github.com/e-letter/e-letter-web) | [Full Documentation](https://github.com/e-letter/e-letter-web#readme)

---

## 🖥️ Desktop Application

A powerful desktop application for managing school permission letters with modern Fluent Design WPF interface. Features client-server architecture with an optional SQLite cache for offline support.

### Desktop Features

- **Modern WPF Design** - Custom gradient themes with smooth transitions
- **Intuitive Navigation** - Easy-to-use menu system for all user roles
- **Professional Styling** - WPF-UI framework with custom controls
- **Role-Based Access** - Student, Teacher, and Administrator portals
- **Permission Management** - Create, track, and manage all letter types
- **Letter Tracking** - Real-time status of permission requests
- **Comprehensive History** - Complete audit trail of all actions
- **Local Storage** - Secure JSON-based data persistence
- **Offline Support** - SQLite cache for offline data access
- **Push Notifications** - Windows Toast notifications for status updates
- **Windows Native** - .NET Framework 4.7.2 compatibility

### Desktop Tech Stack

| Component         | Technology                             |
| ----------------- | -------------------------------------- |
| **Platform**      | Windows Desktop (.NET Framework 4.7.2) |
| **Language**      | C# 10.0                                |
| **UI Framework**  | WPF (Windows Presentation Foundation)  |
| **UI Library**    | WPF-UI 4.2.1                           |
| **Pattern**       | MVVM with two-way data binding         |
| **Serialization** | Newtonsoft.Json 13.0.4                 |
| **Networking**    | HttpClient with bearer token auth      |
| **Local DB**      | SQLite (optional, for offline mode)    |
| **Notifications** | Windows Toast                          |

### Desktop Quick Start

```bash
# Clone repository
git clone https://github.com/e-letter/e-letter-desktop.git
cd e-letter-desktop

# Open solution in Visual Studio
start e-letter.sln
# Build > Build Solution (Ctrl+Shift+B)
# Debug > Start Debugging (F5)
```

**Terminal 1** — Start Go backend (from `backend/` folder):

```bash
go run cmd/api/main.go
```

### Desktop Supported Views

- Home Screen - Dashboard and navigation menu
- Permission Forms - Create entry and exit letters
- Letter Tracking - View and manage all letters
- Student Registry - Manage student information
- Teacher Registry - Manage teacher information
- Check-in System - Student and teacher attendance tracking
- Dispensation Management - Special permission handling

👉 [View Desktop Project](https://github.com/e-letter/e-letter-desktop) | [Full Documentation](https://github.com/e-letter/e-letter-desktop#readme)

---

## 📱 Mobile Application

A powerful Android application for managing school permission letters with native mobile interface and seamless user experience. Built with Kotlin and Android Jetpack with Material Design 3.

### Mobile Features

- **Material Design 3** - Modern, intuitive interface optimized for mobile
- **Role-Based Access** - Student App and Teacher App with different dashboards
- **Permission Management** - Create, submit, and track letters on-the-go
- **Real-Time Notifications** - Push notifications for approval status updates
- **Offline Support** - Basic functionality available without internet (Room DB pending)
- **Biometric Authentication** - Support for fingerprint and face recognition (pending)
- **Letter Tracking** - Track submitted letters with real-time status
- **Responsive Design** - Perfect display on phones and tablets

### Mobile Tech Stack

| Component        | Technology                          |
| ---------------- | ----------------------------------- |
| **Platform**     | Android 8+ (minSdk 24)              |
| **Language**     | Kotlin 2.0                          |
| **UI Framework** | Android Jetpack + Material Design 3 |
| **Database**     | Room Database (local persistence)   |
| **Networking**   | Retrofit 2 + OkHttp for API calls   |
| **Auth**         | JWT with SharedPreferences          |
| **Logging**      | HttpLoggingInterceptor (HTTP debug) |

### Mobile Quick Start

```bash
git clone https://github.com/e-letter/e-letter-android.git
cd e-letter-android
# Open in Android Studio
# File > Sync Now > Run > Run 'app'
```

### Mobile Key Screens

- Welcome/Login - Authentication with role selection
- Student Dashboard - Home, create letter, view letters, tracking
- Teacher Dashboard - Home, review requests, manage approvals
- Permission Forms - Create letters with form validation
- Letter History - View all submitted letters
- Profile Management - User profile and settings
- Notifications - Real-time approval updates

👉 [View Mobile Project](https://github.com/e-letter/e-letter-android) | [Full Documentation](https://github.com/e-letter/e-letter-android#readme)

---

## 🔄 User Workflows

### Student Workflow

```text
Register/Login
     ↓
Select Permission Type
     ↓
Fill Permission Form
     ↓
Submit Request
     ↓
Track Approval Status
     ↓
Receive Approval/Rejection
```

**Available on**: 🌐 Web | 🖥️ Desktop | 📱 Mobile

### Teacher Workflow

```text
Login
     ↓
View Pending Requests
     ↓
Review Student Information
     ↓
Approve/Reject/Request Info
     ↓
Add Comments & Signatures
     ↓
Notify Student of Decision
```

**Available on**: 🌐 Web | 🖥️ Desktop | 📱 Mobile

### Administrator Workflow

```text
Login
     ↓
Manage Users
     ↓
Configure Workflows
     ↓
View System Reports
     ↓
Monitor Audit Logs
     ↓
Maintain Settings
```

**Available on**: 🌐 Web | 🖥️ Desktop

---

## 🔐 Security & Authentication

### Common Security Features

- **Role-Based Access Control** - Fine-grained permission management
- **Secure Password Storage** - bcrypt hashing (Web/Backend), secure storage (Desktop/Mobile)
- **Session Management** - Secure session creation and tracking
- **Audit Logging** - Complete history of all actions
- **Token-Based Authentication** - JWT for web, session tokens for desktop/mobile

### Platform-Specific Security

| Feature               | Web | Desktop | Mobile |
| --------------------- | --- | ------- | ------ |
| JWT Authentication    | ✅  | ✅      | ✅     |
| Refresh Tokens        | ✅  | ✅      | -      |
| Local Session Storage | ✅  | ✅      | ✅     |
| HTTPS Only            | ✅  | -       | -      |
| Encrypted Preferences | -   | -       | -      |
| Biometric Auth        | -   | -       | 🔜     |

### User Role Hierarchy

```text
ADMIN
├── Full system access
├── Manage users & permissions
└── View all reports

KEPSEK (Principal)
├── Override approval authority
├── View institution statistics
└── Override approval stages

GURU_KESISWAAN (Discipline Teacher)
├── Review student requests
├── Approve/reject letters
└── Add digital signatures

GURU_MAPEL (Subject Teacher)
├── Review assigned student requests
├── Approve/forward to higher role
└── Manage class activities

SISWA (Student)
├── Submit permission requests
├── Track request status
└── View approval comments
```

### Sub-Roles for Teachers

Guru dapat memiliki beberapa sub-role yang menentukan cakupan persetujuan:

| Peran          | Deskripsi               | Cakupan Persetujuan       |
| -------------- | ----------------------- | ------------------------- |
| **Wali Kelas** | Guru kelas              | Siswa kelasnya sendiri    |
| **Kapro**      | Kepala program keahlian | Siswa di jurusannya       |
| **Tatib**      | Guru tata tertib        | Semua siswa (tahap akhir) |
| **Guru Mapel** | Guru mata pelajaran     | Siswa di jadwalnya        |

---

## 📊 Features Comparison

| Feature                   | Web | Desktop | Mobile  |
| ------------------------- | --- | ------- | ------- |
| Create Permission Letters | ✅  | ✅      | ✅      |
| Track Letter Status       | ✅  | ✅      | ✅      |
| Teacher Review/Approval   | ✅  | ✅      | ✅      |
| Admin Management          | ✅  | ✅      | -       |
| Real-Time Updates         | ✅  | -       | ✅      |
| Beautiful UI              | ✅  | ✅      | ✅      |
| Offline Support           | -   | ✅      | Partial |
| Mobile Optimized          | ✅  | -       | ✅      |
| Export Reports            | ✅  | ✅      | -       |
| Database Persistence      | ✅  | ✅      | ✅      |

---

## 🗄️ Database Architecture

### Backend Database (MariaDB)

Shared by Web and Desktop clients via Go API. Organized into **6 logical sections**:

```text
┌─────────────────────────────────────────────────────────────┐
│            1. TABEL REFERENSI UTAMA                         │
│  (ref_values, academic_years, majors, classes, subjects)    │
└─────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────┐
│            2. TABEL MANAJEMEN PENGGUNA                      │
│  (users, student_profiles, teacher_profiles, principals)    │
└─────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────┐
│        3. TABEL ORGANISASI AKADEMIK                         │
│  (teacher_roles, class_assignments, schedules)              │
└─────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────┐
│       4. TABEL SISTEM PERMOHONAN & PERSETUJUAN              │
│  (requests, request_approvals, approval_flow_templates)     │
└─────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────┐
│            5. TABEL PENDUKUNG                               │
│  (attachments, notifications, letter_counters)              │
└─────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────┐
│         6. TABEL AUDIT & KEAMANAN                           │
│  (jwt_tokens, audit_logs, password_reset_tokens)            │
└─────────────────────────────────────────────────────────────┘
```

### Key Tables

| Table                     | Purpose                             | Key Fields                                    |
| ------------------------- | ----------------------------------- | --------------------------------------------- |
| `users`                   | User accounts                       | `id`, `username/email`, `role`, `status`      |
| `student_profiles`        | Student profile data                | `user_id`, `student_code` (NISN), `signature` |
| `teacher_profiles`        | Teacher profile data                | `user_id`, `employee_code` (NIP), `signature` |
| `teacher_roles`           | Teacher sub-roles per academic year | `teacher_id`, `role_name`, `status`           |
| `requests`                | Permission letter requests          | `request_number`, `type_id`, `status`         |
| `request_approvals`       | Approval workflow steps             | `request_id`, `step_no`, `approver_role`      |
| `approval_flow_templates` | Configurable approval templates     | `type_id`, `step_no`, `approver_role`         |
| `jwt_tokens`              | JWT token storage & revocation      | `user_id`, `token_hash`, `is_revoked`         |

### Client-Side Cache (SQLite — Desktop & Mobile)

| Table           | Purpose                                      |
| --------------- | -------------------------------------------- |
| `local_letters` | Letters created offline (pending sync)       |
| `sync_queue`    | Operation queue for deferred synchronization |
| `cached_users`  | Cached reference/master data                 |

---

## 🔌 API Reference

### Base URL

```text
http://localhost:8080/api/v1
```

### Authentication Endpoints

| Endpoint        | Method | Description          |
| --------------- | ------ | -------------------- |
| `/auth/login`   | POST   | User login           |
| `/auth/logout`  | POST   | User logout          |
| `/auth/refresh` | POST   | Refresh access token |
| `/register`     | POST   | Register with token  |

### User Endpoints

| Endpoint        | Method | Description         |
| --------------- | ------ | ------------------- |
| `/user/profile` | GET    | Get user profile    |
| `/user/update`  | POST   | Update user profile |

### Permission Request Endpoints

| Endpoint               | Method | Description               |
| ---------------------- | ------ | ------------------------- |
| `/permission-requests` | GET    | List permission requests  |
| `/permission-requests` | POST   | Create permission request |
| `/permission-requests` | PUT    | Update permission request |
| `/permission-requests` | DELETE | Delete permission request |
| `/approve`             | POST   | Approve/reject request    |

### Letter Endpoints

| Endpoint                       | Method | Description             |
| ------------------------------ | ------ | ----------------------- |
| `/letters/student/create`      | POST   | Create student letter   |
| `/letters/teacher/create`      | POST   | Create teacher letter   |
| `/letters/student/izin-masuk`  | GET    | Get izin masuk letters  |
| `/letters/student/izin-keluar` | GET    | Get izin keluar letters |
| `/letters/student/dispensasi`  | GET    | Get dispensasi letters  |

### Client Credentials (Development)

| Role        | Email      | Password | Dashboard         |
| ----------- | ---------- | -------- | ----------------- |
| **Student** | `123`      | `12345`  | Student Dashboard |
| **Teacher** | `G123`     | `12345`  | Teacher Dashboard |
| **Admin**   | `admin123` | `12345`  | Admin Panel       |

---

## 🎨 Design System

All platforms follow a consistent, modern design language with gradient themes and glassmorphism effects.

### Color Palette

| Type             | Primary Color | Gradient            |
| ---------------- | ------------- | ------------------- |
| Entry/Izin Masuk | Purple        | `#C471ED → #F64F59` |
| Exit/Izin Keluar | Orange        | `#FDC830 → #F37335` |
| Dispensation     | Blue          | `#2193b0 → #6dd5ed` |

### Typography

| Context       | Web       | Desktop  | Mobile |
| ------------- | --------- | -------- | ------ |
| **Body Text** | Nunito    | System   | Roboto |
| **Headings**  | Quicksand | Segoe UI | Roboto |

### Component Patterns

- **Interactive Cards** - Selectable with visual feedback
- **Smooth Animations** - Framer Motion (Web), WPF (Desktop), Material (Mobile)
- **Glassmorphism** - Modern backdrop blur effects
- **Responsive Layouts** - Adapts to all screen sizes

---

## 🛠️ Development Setup

### Environment Variables (Web)

```env
# Database
DB_HOST=localhost
DB_PORT=3306
DB_USER=eletter_user
DB_PASSWORD=your_password
DB_NAME=db_eletter

# JWT Secrets
JWT_ACCESS_SECRET=your_access_secret
JWT_REFRESH_SECRET=your_refresh_secret

# Application
NODE_ENV=development
APP_ENV=development
APP_PORT=8080
```

### Environment Variables (Desktop — `App.config`)

```xml
<appSettings>
  <add key="ApiBaseUrl" value="http://localhost:8080/api/v1" />
  <add key="TimeoutSeconds" value="30" />
  <add key="EnableOfflineMode" value="true" />
  <add key="MaxRetryAttempts" value="3" />
</appSettings>
```

### Environment Variables (Backend Go — `.env`)

```env
DB_HOST=localhost
DB_PORT=3306
DB_USER=eletter_user
DB_PASSWORD=your_password
DB_NAME=db_eletter
JWT_ACCESS_SECRET=your_access_secret
JWT_REFRESH_SECRET=your_refresh_secret
```

---

## 📱 Mobile Setup Details

### Prasyarat

- **Android Studio** (Arctic Fox atau lebih baru)
- **JDK 11** atau lebih baru
- **Android SDK** API Level 24 (minSdk 24) — Android 7.0+
- **Kotlin** 2.0.21
- **Server Backend** berjalan di `http://192.168.1.6:3000/`

### Konfigurasi API Base URL

Ubah `BASE_URL` di `RetrofitClient.kt`:

```kotlin
private const val BASE_URL = "http://192.168.1.6:3000/"
```

### Menjalankan Build

```bash
# Build dan install
./gradlew installDebug
# Atau melalui Android Studio: Build > Run 'app'
```

---

## 📞 Support & Links

[🌐 Web App](https://github.com/e-letter/e-letter-web) · [🖥️ Desktop App](https://github.com/e-letter/e-letter-desktop) · [📱 Mobile App](https://github.com/e-letter/e-letter-android)

[Report Bug](https://github.com/e-letter/e-letter-web/issues) · [Request Feature](https://github.com/e-letter/e-letter-web/issues) · [Discussions](https://github.com/e-letter/e-letter-web/discussions)

---

## 🙏 Acknowledgments

### Built With

#### Web

- [Next.js](https://nextjs.org/) - React framework
- [Tailwind CSS](https://tailwindcss.com/) - Styling
- [Framer Motion](https://www.framer.com/motion/) - Animations
- [shadcn/ui](https://ui.shadcn.com/) - UI components

#### Desktop

- [WPF-UI](https://github.com/lepoco/wpfui) - Modern WPF controls
- [Newtonsoft.Json](https://www.newtonsoft.com/json) - JSON serialization
- [.NET Framework](https://dotnet.microsoft.com/) - Runtime

#### Mobile

- [Android Jetpack](https://developer.android.com/jetpack) - Framework
- [Material Design 3](https://material.io/) - Design system
- [Retrofit2](https://square.github.io/retrofit/) - Networking
- [Room Database](https://developer.android.com/jetpack/androidx/releases/room) - Persistence

### Special Thanks

- The open-source community for amazing tools and libraries
- All contributors and supporters of the E-Letter project

---

## 📄 License

**Proprietary License** - All Rights Reserved

All E-Letter repositories are available for:

- ✅ Viewing and educational purposes
- ✅ Contributing via Pull Requests
- ✅ Internal organizational use

Prohibited without explicit permission:

- ❌ Redistribution
- ❌ Creating derivative works
- ❌ Commercial use
- ❌ Removing copyright notices

---

## 🏢 Organization Structure

```text
E-Letter Organization
│
├── 🌐 e-letter-web (Website)
│   ├── Next.js 16 + TypeScript
│   ├── Tailwind CSS 4 + shadcn/ui
│   ├── Framer Motion (Animations)
│   ├── MariaDB 11.5 Database
│   ├── Go 1.22 + Gin Backend API
│   └── Docker & Docker Compose
│
├── 🖥️ e-letter-desktop (Windows)
│   ├── .NET Framework 4.7.2 + WPF
│   ├── WPF-UI 4.2.1 (Fluent Design)
│   ├── MVVM Architecture
│   ├── Newtonsoft.Json 13.0.4
│   ├── SQLite (Offline Cache)
│   └── Windows Toast Notifications
│
└── 📱 e-letter-android (Mobile)
    ├── Android 14+ / Kotlin 2.0
    ├── Material Design 3
    ├── Android Jetpack Framework
    ├── Retrofit 2 + OkHttp
    ├── Room Database (pending)
    └── Biometric Auth (pending)
```

---

## 🚀 Future Roadmap

- [ ] **Mobile offline mode** — Room Database caching for Android
- [ ] **Push notifications** — Firebase Cloud Messaging integration
- [ ] **Biometric authentication** — Fingerprint & face recognition (Mobile)
- [ ] **Photo/document attachments** — Camera/gallery integration (Mobile)
- [ ] **PDF generation & download** — Approved letter export
- [ ] **Multi-language support** — Internationalization (i18n)
- [ ] **Dark theme toggle** — Explicit dark/light mode switch (Mobile)
- [ ] **Jetpack Compose migration** — Modern UI toolkit for Android

---

Simplifying school permission letter management across all platforms
