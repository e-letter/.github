# E-Letter Organization 📝

> **Complete school permission letter management system** across web, desktop, and mobile platforms with modern interfaces, seamless user experience, and comprehensive letter tracking.

[![Website](https://img.shields.io/badge/Web-Next.js%2016-000?logo=next.js)](https://github.com/e-letter/e-letter-web)
[![Desktop](https://img.shields.io/badge/Desktop-.NET%204.7.2-512BD4?logo=dot-net)](https://github.com/e-letter/e-letter-desktop)
[![Mobile](https://img.shields.io/badge/Mobile-Android%20Java-3DDC84?logo=android)](https://github.com/e-letter/e-letter-android)

## 📊 Platform Overview

| Platform   | Framework                 | Language   | Key Features                                           | Repository                                                       |
| ---------- | ------------------------- | ---------- | ------------------------------------------------------ | ---------------------------------------------------------------- |
| 🌐 Web     | Next.js 16 + Tailwind CSS | TypeScript | Real-time tracking, Multi-stage approval, Beautiful UI | [e-letter-web](https://github.com/e-letter/e-letter-web)         |
| 🖥️ Desktop | .NET 4.7.2 + WPF          | C#         | Offline support, Local storage, Native Windows         | [e-letter-desktop](https://github.com/e-letter/e-letter-desktop) |
| 📱 Mobile  | Android 11+               | Java       | Mobile-optimized, Push notifications, Biometric auth   | [e-letter-android](https://github.com/e-letter/e-letter-android) |

---

## 🎯 About E-Letter

E-Letter is a comprehensive **school permission letter management system** designed to streamline managing student permission requests across multiple platforms.

### Core Capabilities

- **Multi-Platform Access** - Web, Desktop, and Mobile with unified workflows
- **Role-Based Access Control** - Students, Teachers, and Administrators with tailored dashboards
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

A modern, interactive web application for managing school permission letters with beautiful UI and seamless user experience.

[![Next.js](https://img.shields.io/badge/Next.js-16.0-black?logo=next.js)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue?logo=typescript)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-4.0-38bdf8?logo=tailwind-css)](https://tailwindcss.com/)
[![MariaDB](https://img.shields.io/badge/MariaDB-11.5-003545?logo=mariadb)](https://mariadb.org/)

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

### Web Quick Start

```bash
git clone https://github.com/e-letter/e-letter-web.git
cd e-letter-web
bun install
cp .env.example .env.local
docker-compose up -d
bun dev
```

### Web Tech Stack

- **Framework**: Next.js 16 (App Router)
- **Language**: TypeScript 5
- **Styling**: Tailwind CSS 4 + Framer Motion
- **UI Library**: shadcn/ui components
- **Database**: MariaDB 11.5
- **Authentication**: JWT with access/refresh tokens
- **Deployment**: Docker & Docker Compose

### Web Database Architecture

The database uses **5 logical sections**:

1. **Reference Tables** - Roles, majors, classes, permission types
2. **User Management** - Users, profiles, authentication tokens
3. **Permission System** - Requests, approval stages, approval logs
4. **Supporting Data** - Dispensations, attachments, letter sequences
5. **Audit & Logging** - Login logs, system audit trails

Key tables: `users`, `permission_requests`, `approval_stages`, `permission_approval_logs`, `dispensation_students`

👉 [View Web Project](https://github.com/e-letter/e-letter-web) | [Documentation](https://github.com/e-letter/e-letter-web#readme)

---

## 🖥️ Desktop Application

A powerful desktop application for managing school permission letters with modern WPF interface and seamless user experience.

[![.NET Framework](https://img.shields.io/badge/.NET%20Framework-4.7.2-512BD4?logo=dot-net)](https://dotnet.microsoft.com/download/dotnet-framework)
[![WPF](https://img.shields.io/badge/WPF-UI%204.1-0078D4?logo=windows)](https://github.com/lepoco/wpfui)
[![C#](https://img.shields.io/badge/C%23-10.0-239120?logo=csharp)](https://docs.microsoft.com/en-us/dotnet/csharp/)

### Desktop Features

- **Modern WPF Design** - Custom gradient themes with smooth transitions
- **Intuitive Navigation** - Easy-to-use menu system for all user roles
- **Professional Styling** - WPF-UI framework with custom controls
- **Role-Based Access** - Student, Teacher, and Administrator portals
- **Permission Management** - Create, track, and manage all letter types
- **Letter Tracking** - Real-time status of permission requests
- **Comprehensive History** - Complete audit trail of all actions
- **Local Storage** - Secure JSON-based data persistence
- **Windows Native** - .NET Framework 4.7.2 compatibility

### Desktop Quick Start

```bash
git clone https://github.com/e-letter/e-letter-desktop.git
cd e-letter-desktop
start e-letter.sln
# Build > Build Solution (Ctrl+Shift+B)
# Debug > Start Debugging (F5)
```

### Desktop Tech Stack

- **Platform**: Windows Desktop (.NET Framework 4.7.2)
- **Language**: C# 10.0
- **UI Framework**: WPF (Windows Presentation Foundation)
- **UI Library**: WPF-UI 4.1
- **Serialization**: Newtonsoft.Json 13.0.4
- **Data Format**: JSON with local storage

### Desktop Supported Views

- Home Screen - Dashboard and navigation menu
- Permission Forms - Create entry and exit letters
- Letter Tracking - View and manage all letters
- Student Registry - Manage student information
- Teacher Registry - Manage teacher information
- Check-in System - Student and teacher attendance tracking
- Dispensation Management - Special permission handling

👉 [View Desktop Project](https://github.com/e-letter/e-letter-desktop) | [Documentation](https://github.com/e-letter/e-letter-desktop#readme)

---

## 📱 Mobile Application

A powerful Android application for managing school permission letters with native mobile interface and seamless user experience.

[![Android](https://img.shields.io/badge/Android-8+-3DDC84?logo=android)](https://www.android.com/)
[![Java](https://img.shields.io/badge/Java-17+-007396?logo=java)](https://www.oracle.com/java/)
[![Material Design](https://img.shields.io/badge/Material%20Design-3-757575?logo=material-design)](https://material.io/)

### Mobile Features

- **Material Design 3** - Modern, intuitive interface optimized for mobile
- **Role-Based Access** - Student App and Teacher App with different dashboards
- **Permission Management** - Create, submit, and track letters on-the-go
- **Real-Time Notifications** - Push notifications for approval status updates
- **Offline Support** - Basic functionality available without internet
- **Biometric Authentication** - Support for fingerprint and face recognition
- **Letter Tracking** - Track submitted letters with real-time status
- **Responsive Design** - Perfect display on phones and tablets

### Mobile Quick Start

```bash
git clone https://github.com/e-letter/e-letter-android.git
cd e-letter-android
start .
# File > Sync Now
# Run > Run 'app'
```

### Mobile Tech Stack

- **Platform**: Android 8+
- **Language**: Java 17+
- **UI Framework**: Android Jetpack with Material Design 3
- **Database**: Room Database (local persistence)
- **Networking**: Retrofit2 for API communication
- **Authentication**: JWT with SharedPreferences

### Mobile Key Screens

- Welcome/Login - Authentication with role selection
- Student Dashboard - Home, create letter, view letters, tracking
- Teacher Dashboard - Home, review requests, manage approvals
- Permission Forms - Create letters with form validation
- Letter History - View all submitted letters
- Profile Management - User profile and settings
- Notifications - Real-time approval updates

👉 [View Mobile Project](https://github.com/e-letter/e-letter-android) | [Documentation](https://github.com/e-letter/e-letter-android#readme)

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
- **Secure Password Storage** - bcryptjs hashing (Web), secure storage (Desktop/Mobile)
- **Session Management** - Secure session creation and tracking
- **Audit Logging** - Complete history of all actions
- **Token-Based Authentication** - JWT for web, session tokens for desktop/mobile

### Platform-Specific Security

| Feature               | Web | Desktop | Mobile |
| --------------------- | --- | ------- | ------ |
| JWT Authentication    | ✅  | ✅       | -      |
| Refresh Tokens        | ✅  | ✅      | -      |
| Local Session Storage | ✅  | ✅      | -      |
| HTTPS Only            | ✅  | -       | -      |
| Encrypted Preferences | -   | -       | -      |

### User Role Hierarchy

```text
ADMIN
├── Full system access
├── Manage users & permissions
└── View all reports

KEPSEK (Principal)
├── Final approval authority
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

## 🎨 Design System

All platforms follow a consistent, modern design language.

### Color Palette

| Permission Type    | Primary Color | Gradient            |
| ------------------ | ------------- | ------------------- |
| Entry (Izin Masuk) | Purple        | `#C471ED → #F64F59` |
| Exit (Izin Keluar) | Orange        | `#FDC830 → #F37335` |
| Dispensation       | Blue          | `#2193b0 → #6dd5ed` |

### Typography

- **Body Text**: Nunito (Web), System (Desktop/Mobile)
- **Headings**: Quicksand (Web), Segoe UI (Desktop), Roboto (Mobile)

### Component Patterns

- **Interactive Cards** - Selectable with visual feedback
- **Smooth Animations** - Framer Motion (Web), WPF (Desktop), Material (Mobile)
- **Glassmorphism** - Modern backdrop blur effects
- **Responsive Layouts** - Adapts to all screen sizes

---

## 📚 Getting Started

### Choose Your Platform

**🌐 Building the Web App?**

Go to [e-letter-web](https://github.com/e-letter/e-letter-web)

- Tech: Next.js 16, TypeScript, Tailwind CSS, MariaDB
- [Quick Start Guide](https://github.com/e-letter/e-letter-web#readme)

**🖥️ Building the Desktop App?**

Go to [e-letter-desktop](https://github.com/e-letter/e-letter-desktop)

- Tech: .NET 4.7.2, C#, WPF
- [Quick Start Guide](https://github.com/e-letter/e-letter-desktop#readme)

**📱 Building the Mobile App?**

Go to [e-letter-android](https://github.com/e-letter/e-letter-android)

- Tech: Android, Java, Material Design 3
- [Quick Start Guide](https://github.com/e-letter/e-letter-android#readme)

### Development Workflow

1. Choose a repository above
2. Clone the repository
3. Install dependencies
4. Configure environment
5. Run development server
6. Start contributing!

---

## 🤝 Contributing

Contributions are welcome across all platforms! Please follow these guidelines:

1. Fork the repository of your choice
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Make your changes following code style guidelines
4. Test thoroughly on your target platform
5. Commit with clear, descriptive messages
6. Push to your fork
7. Open a Pull Request

### Code Style Guidelines

#### TypeScript/React (Web)

- Use TypeScript for type safety
- Follow existing component patterns
- Use Tailwind CSS utilities
- Add comments for complex logic

#### C# (Desktop)

- Use PascalCase for classes and methods
- Keep methods small and focused
- Add meaningful comments
- Follow existing UI patterns

#### Java (Mobile)

- Use consistent naming conventions
- Add proper error handling
- Follow Material Design principles
- Document complex logic

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
│   ├── Tailwind CSS + shadcn/ui
│   ├── MariaDB Database
│   └── Docker Deployment
│
├── 🖥️ e-letter-desktop (Windows)
│   ├── .NET Framework 4.7.2
│   ├── C# with WPF-UI
│   ├── Local JSON Storage
│   └── Windows Native
│
└── 📱 e-letter-android (Mobile)
    ├── Android 11+ (Java)
    ├── Material Design 3
    ├── Room Database
    └── Mobile Optimized
```

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

## 📞 Support & Links

[🌐 Web App](https://github.com/e-letter/e-letter-web) · [🖥️ Desktop App](https://github.com/e-letter/e-letter-desktop) · [📱 Mobile App](https://github.com/e-letter/e-letter-android)

[Report Bug](https://github.com/e-letter/e-letter-web/issues) · [Request Feature](https://github.com/e-letter/e-letter-web/issues) · [Discussions](https://github.com/e-letter/e-letter-web/discussions)

---

Simplifying school permission letter management across all platforms
