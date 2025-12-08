# E-Letter Organization 📝

> **Complete school permission letter management system** across web, desktop, and mobile platforms with modern interfaces, seamless user experience, and comprehensive letter tracking.

<div align="center">

[![Website](https://img.shields.io/badge/Web-Next.js%2016-000?logo=next.js)](https://github.com/e-letter/e-letter-web)
[![Desktop](https://img.shields.io/badge/Desktop-.NET%204.7.2-512BD4?logo=dot-net)](https://github.com/e-letter/e-letter-desktop)
[![Mobile](https://img.shields.io/badge/Mobile-Android%20Java-3DDC84?logo=android)](https://github.com/e-letter/e-letter-android)

| **Platform** | **Framework**    | **Language** | **Repository**                                                   |
| ------------ | ---------------- | ------------ | ---------------------------------------------------------------- |
| 🌐 Website   | Next.js 16       | TypeScript   | [e-letter-website](https://github.com/e-letter/e-letter-web)                 |
| 🖥️ Desktop   | .NET 4.7.2 / WPF | C#           | [e-letter-desktop](https://github.com/e-letter/e-letter-desktop) |
| 📱 Mobile    | Android          | Java         | [e-letter-android](https://github.com/e-letter/e-letter-android) |

</div>

---

## 🎯 About E-Letter

E-Letter is a comprehensive **school permission letter management system** designed to streamline the process of managing student permission requests. The system provides:

- **Multi-Platform Access** - Web, Desktop, and Mobile applications
- **Role-Based Management** - Students, Teachers, and Administrators with tailored dashboards
- **Real-Time Tracking** - Live status updates on permission requests
- **Beautiful UI** - Modern, gradient-based interfaces across all platforms
- **Secure Authentication** - Role-based access control and JWT authentication
- **Complete Audit Trail** - Comprehensive history and logging of all actions

### Supported Permission Types

| Type                 | Code        | Description                                               | Use Case                            |
| -------------------- | ----------- | --------------------------------------------------------- | ----------------------------------- |
| **Entry Permission** | Izin Masuk  | Permission for late arrival or after-absence entry        | Student arrives late to school      |
| **Exit Permission**  | Izin Keluar | Permission to leave school premises during school hours   | Student needs to leave early        |
| **Dispensation**     | Dispensasi  | Special exemptions from school activities or requirements | Medical reasons, family emergencies |

---

## 🌐 Web Application

> A modern, interactive web application for managing school permission letters with a beautiful UI and seamless user experience.

[![Next.js](https://img.shields.io/badge/Next.js-16.0-black?logo=next.js)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue?logo=typescript)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-4.0-38bdf8?logo=tailwind-css)](https://tailwindcss.com/)
[![MariaDB](https://img.shields.io/badge/MariaDB-11.5-003545?logo=mariadb)](https://mariadb.org/)

### ✨ Key Features

- **Beautiful Modern UI** - Gradient design system with glassmorphism effects
- **Role-Based Access** - Student Portal, Teacher Dashboard, Admin Panel
- **Real-Time Tracking** - Live status updates on permission requests
- **Multi-Stage Approval** - Workflow with student, teacher, and disciplinary signatures
- **JWT Authentication** - Secure token-based authentication with refresh tokens
- **Fully Responsive** - Works perfectly on all devices
- **Docker Ready** - One-command deployment

### 🚀 Quick Start

```bash
# Clone repository
git clone https://github.com/e-letter/e-letter-web.git
cd e-letter-web

# Install dependencies
bun install

# Set up environment
cp .env.example .env.local

# Start database
docker-compose up -d

# Run development server
bun dev
```

### 🏗️ Tech Stack

- **Framework**: Next.js 16 (App Router)
- **Language**: TypeScript 5
- **Styling**: Tailwind CSS 4 + Framer Motion
- **UI Library**: shadcn/ui components
- **Database**: MariaDB 11.5
- **Authentication**: JWT with access/refresh tokens
- **Deployment**: Docker & Docker Compose

👉 **[View Web Project](https://github.com/e-letter/e-letter-web.git)** | **[Documentation](https://github.com/e-letter/e-letter-web#readme)**

---

## 🖥️ Desktop Application

> A powerful desktop application for managing school permission letters with a modern WPF interface and seamless user experience.

[![.NET Framework](https://img.shields.io/badge/.NET%20Framework-4.7.2-512BD4?logo=dot-net)](https://dotnet.microsoft.com/download/dotnet-framework)
[![WPF](https://img.shields.io/badge/WPF-UI%204.1-0078D4?logo=windows)](https://github.com/lepoco/wpfui)
[![C#](https://img.shields.io/badge/C%23-Modern-239120?logo=csharp)](https://docs.microsoft.com/en-us/dotnet/csharp/)

### ✨ Key Features

- **Role-Based Access** - Student Portal, Teacher Dashboard, Administrator Panel
- **Permission Management** - Create, track, and manage permission letters
- **Intuitive Interfaces** - Clean, user-friendly Windows desktop application
- **Letter Tracking** - Real-time status of all permission requests
- **Comprehensive History** - Complete audit trail of all actions
- **Local Storage** - Secure JSON-based data persistence
- **Modern UI** - WPF with custom styling and smooth animations

### 🚀 Quick Start

```bash
# Clone repository
git clone https://github.com/e-letter/e-letter-desktop.git
cd e-letter-desktop

# Open in Visual Studio 2019+
start e-letter.sln

# Build solution
Build > Build Solution (Ctrl+Shift+B)

# Run application
Debug > Start Debugging (F5)
```

### 🏗️ Tech Stack

- **Platform**: Windows Desktop
- **Framework**: .NET Framework 4.7.2
- **Language**: C# 10.0
- **UI Framework**: WPF (Windows Presentation Foundation)
- **UI Library**: WPF-UI 4.1
- **Data Format**: JSON with local storage
- **Dependencies**: Newtonsoft.Json, System libraries

### 📋 Supported Views

- **Home Screen** - Dashboard and navigation menu
- **Permission Forms** - Create entry and exit letters
- **Letter Tracking** - View and manage all letters
- **Student Registry** - Manage student information
- **Teacher Registry** - Manage teacher information
- **Check-in System** - Student and teacher attendance tracking

👉 **[View Desktop Project](https://github.com/e-letter/e-letter-desktop)** | **[Documentation](https://github.com/e-letter/e-letter-desktop#readme)**

---

## 📱 Mobile Application (Android)

> A powerful Android application for managing school permission letters with native mobile interface and seamless user experience.

[![Android](https://img.shields.io/badge/Android-11+-3DDC84?logo=android)](https://www.android.com/)
[![Java](https://img.shields.io/badge/Java-17+-007396?logo=java)](https://www.oracle.com/java/)
[![Material Design](https://img.shields.io/badge/Material%20Design-3-757575?logo=material-design)](https://material.io/)

### ✨ Key Features

- **Role-Based Access** - Student App, Teacher App, with different dashboards
- **Permission Management** - Create, submit, and track permission letters on-the-go
- **Mobile-Optimized UI** - Material Design 3 interface optimized for mobile devices
- **Real-Time Notifications** - Push notifications for approval status updates
- **Offline Support** - Basic functionality available even without internet
- **Biometric Authentication** - Support for fingerprint and face recognition
- **Letter Tracking** - Track all submitted letters with real-time status updates
- **Responsive Design** - Perfect display on phones and tablets

### 🚀 Quick Start

```bash
# Clone repository
git clone https://github.com/e-letter/e-letter-android.git
cd e-letter-android

# Open in Android Studio
start .

# Sync Gradle dependencies
File > Sync Now

# Run on emulator or device
Run > Run 'app'
```

### 🏗️ Tech Stack

- **Platform**: Android 11+
- **Language**: Java 17+
- **UI Framework**: Android Jetpack with Material Design 3
- **Database**: Room Database (local persistence)
- **Networking**: Retrofit2 for API communication
- **Authentication**: JWT with SharedPreferences
- **Dependencies**: Material Design, OkHttp, GSON

### 📋 Key Screens

- **Welcome/Login** - Authentication screen with role selection
- **Student Dashboard** - Home, create letter, view letters, tracking
- **Teacher Dashboard** - Home, review requests, manage approvals
- **Permission Forms** - Create entry/exit letters with form validation
- **Letter History** - View all submitted letters with detailed information
- **Profile Management** - User profile and settings management
- **Notifications** - Real-time updates on letter approvals

👉 **[View Mobile Project](https://github.com/e-letter/e-letter-android)** | **[Documentation](https://github.com/e-letter/e-letter-android#readme)**

---

## 🔄 Workflow Across Platforms

### For Students

```!/bin/bash
Register/Login
    ↓
Select Permission Type (Entry/Exit/Dispensation)
    ↓
Fill Permission Form
    ↓
Submit Request
    ↓
Track Approval Status (Real-time)
    ↓
Receive Approval/Rejection
```

**Available on**: 🌐 Web | 🖥️ Desktop | 📱 Mobile

### For Teachers

```!/bin/bash
Login
    ↓
View Pending Requests
    ↓
Review Student Information
    ↓
Approve/Reject/Request More Info
    ↓
Add Comments
    ↓
Notify Student of Decision
```

**Available on**: 🌐 Web | 🖥️ Desktop | 📱 Mobile

### For Administrators

```!/bin/bash
Login
    ↓
Manage Users (Students/Teachers)
    ↓
Configure Approval Workflows
    ↓
View System Reports
    ↓
Monitor Audit Logs
    ↓
Maintain System Settings
```

**Available on**: 🌐 Website | 🖥️ Desktop

---

## 🔐 Security & Authentication

### Common Security Features

- **Role-Based Access Control** - Fine-grained permission management
- **Secure Password Storage** - bcryptjs hashing (Website), secure storage (Desktop/Mobile)
- **Session Management** - Secure session creation and tracking
- **Audit Logging** - Complete history of all actions
- **Token-Based Authentication** - JWT for website, session tokens for desktop/mobile

### Platform-Specific Security

| Feature               | Website | Desktop | Mobile |
| --------------------- | ------- | ------- | ------ |
| JWT Authentication    | ✅      | -       | -      |
| Refresh Tokens        | ✅      | -       | -      |
| Local Session Storage | ✅      | ✅      | -      |
| Biometric Auth        | -       | -       | -      |
| HTTPS Only            | ✅      | -       | -      |
| Encrypted Preferences | -       | -       | -      |

---

## 📊 Features Comparison

| Feature                   | Website | Desktop | Mobile  |
| ------------------------- | ------- | ------- | ------- |
| Create Permission Letters | ✅      | ✅      | ✅      |
| Track Letter Status       | ✅      | ✅      | ✅      |
| Teacher Review/Approval   | ✅      | ✅      | ✅      |
| Admin Management          | ✅      | ✅      | -       |
| Real-Time Updates         | ✅      | -       | ✅      |
| Beautiful UI              | ✅      | ✅      | ✅      |
| Offline Support           | -       | ✅      | Partial |
| Mobile Optimized          | ✅      | -       | ✅      |
| Export Reports            | ✅      | ✅      | -       |
| Database Persistence      | ✅      | ✅      | ✅      |

---

## 🎨 Design System

All platforms follow a consistent, modern design language:

### Color Palette

| Permission Type        | Primary Color | Gradient            |
| ---------------------- | ------------- | ------------------- |
| **Entry (Izin Masuk)** | Purple        | `#C471ED → #F64F59` |
| **Exit (Izin Keluar)** | Orange        | `#FDC830 → #F37335` |
| **Dispensation**       | Blue          | `#2193b0 → #6dd5ed` |

### Typography

- **Body Text**: Nunito (Website), System (Desktop/Mobile)
- **Headings**: Quicksand (Website), Segoe UI (Desktop), Roboto (Mobile)

### Component Patterns

- **Interactive Cards** - Selectable with visual feedback
- **Smooth Animations** - Framer Motion (Web), WPF (Desktop), Material (Mobile)
- **Glassmorphism** - Modern backdrop blur effects
- **Responsive Layouts** - Adapts to all screen sizes

---

## 📚 Getting Started

### Choose Your Platform

**🌐 Building the Web App?**

- Go to [e-letter-web](https://github.com/e-letter/e-letter-web.git)
- Tech: Next.js 16, TypeScript, Tailwind CSS, MariaDB

**🖥️ Building the Desktop App?**

- Go to [e-letter-desktop](https://github.com/e-letter/e-letter-desktop)
- Tech: .NET 4.7.2, C#, WPF

**📱 Building the Mobile App?**

- Go to [e-letter-android](https://github.com/e-letter/e-letter-android)
- Tech: Android, Java, Material Design 3

### Development Workflow

1. **Choose a Repository** above
2. **Clone the Repository**
3. **Install Dependencies**
4. **Configure Environment** (API endpoints, database, etc.)
5. **Run Development Server**
6. **Start Contributing!**

---

## 🤝 Contributing

We welcome contributions across all platforms! Please follow these guidelines:

1. **Fork** the repository of your choice
2. **Create** a feature branch (`git checkout -b feature/AmazingFeature`)
3. **Make** your changes following code style guidelines
4. **Test** thoroughly on your target platform
5. **Commit** with clear, descriptive messages
6. **Push** to your fork
7. **Open** a Pull Request

### Code Style Guidelines

**Web (TypeScript/React)**

- Use TypeScript for type safety
- Follow existing component patterns
- Use Tailwind CSS utilities
- Add comments for complex logic

**Desktop (C#)**

- Use PascalCase for classes and methods
- Keep methods small and focused
- Add meaningful comments
- Follow existing UI patterns

**Mobile (Java)**

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

```
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

**Web**

- [Next.js](https://nextjs.org/) - React framework
- [Tailwind CSS](https://tailwindcss.com/) - Styling
- [Framer Motion](https://www.framer.com/motion/) - Animations
- [shadcn/ui](https://ui.shadcn.com/) - UI components

**Desktop**

- [WPF-UI](https://github.com/lepoco/wpfui) - Modern WPF controls
- [Newtonsoft.Json](https://www.newtonsoft.com/json) - JSON serialization
- [.NET Framework](https://dotnet.microsoft.com/) - Runtime

**Mobile**

- [Android Jetpack](https://developer.android.com/jetpack) - Framework
- [Material Design 3](https://material.io/) - Design system
- [Retrofit2](https://square.github.io/retrofit/) - Networking
- [Room Database](https://developer.android.com/jetpack/androidx/releases/room) - Persistence

### Special Thanks

- The open-source community for amazing tools and libraries
- All contributors and supporters of the E-Letter project

---

<div align="center">

### 📞 Support & Links

[🌐 Web App](https://github.com/e-letter/e-letter-web) · [🖥️ Desktop App](https://github.com/e-letter/e-letter-desktop) · [📱 Mobile App](https://github.com/e-letter/e-letter-android)

[Report Bug](https://github.com/e-letter/e-letter-web/issues) · [Request Feature](https://github.com/e-letter/e-letter-web/issues) · [Discussions](https://github.com/e-letter/e-letter-web/discussions)

---

_Simplifying school permission letter management across all platforms_

</div>
