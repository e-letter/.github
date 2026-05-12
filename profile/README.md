# E-Letter Organization 📝

> **Sistem manajemen surat izin sekolah yang lengkap** di seluruh platform web, desktop, dan mobile dengan antarmuka modern, pengalaman pengguna yang mulus, dan pelacakan surat yang komprehensif.

[![Website](https://img.shields.io/badge/Web-Next.js%2016-000?logo=next.js)](https://github.com/e-letter/e-letter-web)
[![Desktop](https://img.shields.io/badge/Desktop-.NET%204.7.2-512BD4?logo=dot-net)](https://github.com/e-letter/e-letter-desktop)
[![Mobile](https://img.shields.io/badge/Mobile-Android%2014-3DDC84?logo=android)](https://github.com/e-letter/e-letter-android)
[![License](https://img.shields.io/badge/License-Proprietary-red)](LICENSE)

---

## 📊 Ringkasan Platform

| Platform   | Framework                 | Bahasa     | Fitur Utama                                                | Repository                                                       |
| ---------- | ------------------------- | ---------- | ---------------------------------------------------------- | ---------------------------------------------------------------- |
| 🌐 Web     | Next.js 16 + Tailwind CSS | TypeScript | Pelacakan real-time, Persetujuan multi-tahap, UI indah     | [e-letter-web](https://github.com/e-letter/e-letter-web)         |
| 🖥️ Desktop | .NET 4.7.2 + WPF          | C#         | Dukungan offline, Penyimpanan lokal, Windows native        | [e-letter-desktop](https://github.com/e-letter/e-letter-desktop) |
| 📱 Mobile  | Android 14+ / Kotlin      | Kotlin     | Dioptimalkan untuk mobile, Notifikasi push, Auth biometrik | [e-letter-android](https://github.com/e-letter/e-letter-android) |

---

## 🎯 Tentang E-Letter

E-Letter adalah **sistem manajemen surat izin sekolah** yang komprehensif, dirancang untuk menyederhanakan pengelolaan permintaan izin siswa di berbagai platform. Dibangun dengan arsitektur dual-backend (API Go + frontend Next.js) dan klien platform native, E-Letter menyediakan pengalaman yang konsisten di Web, Desktop, dan Mobile.

### Kemampuan Inti

- **Akses Multi-Platform** - Web, Desktop, dan Mobile dengan alur kerja yang terpadu
- **Kontrol Akses Berbasis Peran** - Siswa, Guru, Kepala Sekolah, dan Administrator dengan dasbor yang disesuaikan
- **Pelacakan Real-Time** - Pembaruan status langsung pada permintaan izin (web & mobile)
- **Alur Persetujuan Multi-Tahap** - Perutean surat lengkap dengan tanda tangan digital
- **Autentikasi Aman** - Token JWT (web), sesi berbasis token (desktop/mobile)
- **UI Modern yang Indah** - Sistem desain gradien yang konsisten di semua platform
- **Lacak Audit Lengkap** - Riwayat dan pencatatan lengkap semua tindakan

### Jenis Izin

| Jenis       | Kode | Warna     | Deskripsi                                     | Penggunaan                        |
| ----------- | ---- | --------- | --------------------------------------------- | --------------------------------- |
| Izin Masuk  | IM   | 🔵 Ungu   | Kedatangan terlambat atau masuk setelah absen | Siswa datang terlambat ke sekolah |
| Izin Keluar | IK   | 🟠 Oranye | Izin pulang lebih awal                        | Siswa perlu pulang lebih awal     |
| Dispensasi  | DISP | 🟡 Kuning | Pengecualian khusus                           | Keadaan darurat medis/keluarga    |

---

## 🌐 Aplikasi Web

Aplikasi web modern dan interaktif untuk mengelola surat izin sekolah dengan UI yang indah dan pengalaman pengguna yang mulus. Dibangun dengan Next.js 16 App Router, TypeScript, dan backend API berbasis Go.

### Fitur Web

- **Sistem Desain Gradien** - Tema ungu, oranye, kuning, dan biru khusus dengan efek glassmorphism
- **Animasi Halus** - Transisi dan mikro-interaksi yang didukung oleh Framer Motion
- **Desain Responsif** - Sepenuhnya responsif di semua perangkat
- **Dasbor Berbasis Peran** - Portal Siswa, Dasbor Guru, Panel Admin
- **Pelacakan Status Real-Time** - Pembaruan proses persetujuan secara langsung
- **Persetujuan Multi-Tahap** - Alur kerja lengkap dengan jejak audit
- **Tanda Tangan Digital** - Penangkapan tanda tangan berbasis canvas
- **Autentikasi JWT** - Token-based yang aman dengan token refresh
- **Siap Docker** - Deploy dengan satu perintah

### Tumpukan Teknologi Web

| Komponen       | Teknologi                      |
| -------------- | ------------------------------ |
| **Framework**  | Next.js 16 (App Router)        |
| **Bahasa**     | TypeScript 5.0                 |
| **Gaya**       | Tailwind CSS 4 + Framer Motion |
| **Pustaka UI** | Komponen shadcn/ui             |
| **Database**   | MariaDB 11.5                   |
| **Backend**    | Go 1.22 + framework Gin        |
| **Auth**       | JWT dengan token akses/refresh |
| **Deploy**     | Docker & Docker Compose        |

### Mulai Cepat (Web)

```bash
git clone https://github.com/e-letter/e-letter-web.git
cd e-letter-web
bun install
cp .env.example .env.local
docker-compose up -d
bun dev
```

### Arsitektur Database Web

Database web menggunakan **5 bagian logis**:

1. **Tabel Referensi** - Peran, jurusan, kelas, jenis izin
2. **Manajemen Pengguna** - Pengguna, profil, token autentikasi
3. **Sistem Izin** - Permintaan, tahapan persetujuan, log persetujuan
4. **Data Pendukung** - Dispensasi, lampiran, urutan surat
5. **Audit & Pencatatan** - Log masuk, jejak audit sistem

Tabel kunci: `users`, `permission_requests`, `approval_stages`, `permission_approval_logs`, `dispensation_students`

👉 [Lihat Proyek Web](https://github.com/e-letter/e-letter-web) | [Dokumentasi Lengkap](https://github.com/e-letter/e-letter-web#readme)

---

## 🖥️ Aplikasi Desktop

Aplikasi desktop yang kuat untuk mengelola surat izin sekolah dengan antarmuka WPF Fluent Design modern. Menawarkan arsitektur klien-server dengan cache SQLite opsional untuk dukungan offline.

### Fitur Desktop

- **Desain WPF Modern** - Tema gradien khusus dengan transisi yang halus
- **Navigasi Intuitif** - Sistem menu yang mudah digunakan untuk semua peran pengguna
- **Gaya Profesional** - Framework WPF-UI dengan kontrol khusus
- **Akses Berbasis Peran** - Portal Siswa, Guru, dan Administrator
- **Manajemen Izin** - Buat, lacak, dan kelola semua jenis surat
- **Pelacakan Surat** - Status real-time dari permintaan izin
- **Riwayat Lengkap** - Jejak audit lengkap dari semua tindakan
- **Penyimpanan Lokal** - Persistensi data berbasis JSON yang aman
- **Dukungan Offline** - Cache SQLite untuk akses data tanpa koneksi
- **Notifikasi Push** - Notifikasi desktop Windows untuk pembaruan status
- **Windows Native** - Kompatibilitas .NET Framework 4.7.2

### Tumpukan Teknologi Desktop

| Komponen           | Teknologi                              |
| ------------------ | -------------------------------------- |
| **Platform**       | Windows Desktop (.NET Framework 4.7.2) |
| **Bahasa**         | C# 10.0                                |
| **Framework UI**   | WPF (Windows Presentation Foundation)  |
| **Pustaka UI**     | WPF-UI 4.2.1                           |
| **Pola**           | MVVM dengan pengikatan data dua arah   |
| **Serialisasi**    | Newtonsoft.Json 13.0.4                 |
| **Jaringan**       | HttpClient dengan autentikasi bearer   |
| **Database Lokal** | SQLite (opsional, untuk mode offline)  |
| **Notifikasi**     | Windows Toast                          |

### Mulai Cepat (Desktop)

```bash
# Kloning repositori
git clone https://github.com/e-letter/e-letter-desktop.git
cd e-letter-desktop

# Buka solusi di Visual Studio
start e-letter.sln
# Build > Build Solution (Ctrl+Shift+B)
# Debug > Start Debugging (F5)
```

**Terminal 1** — Mulai backend Go (dari folder `backend/`):

```bash
go run cmd/api/main.go
```

### Tampilan Desktop yang Didukung

- Layar Utama - Dasbor dan menu navigasi
- Formulir Izin - Membuat surat izin masuk/keluar
- Pelacakan Surat - Melihat dan mengelola semua surat
- Registrasi Siswa - Mengelola data siswa
- Registrasi Guru - Mengelola data guru
- Sistem Absensi - Pelacakan kehadiran siswa dan guru
- Manajemen Dispensasi - Penanganan izin khusus

👉 [Lihat Proyek Desktop](https://github.com/e-letter/e-letter-desktop) | [Dokumentasi Lengkap](https://github.com/e-letter/e-letter-desktop#readme)

---

## 📱 Aplikasi Mobile

Aplikasi Android yang kuat untuk mengelola surat izin sekolah dengan antarmuka mobile native dan pengalaman pengguna yang mulus. Dibangun dengan Kotlin dan Android Jetpack dengan Material Design 3.

### Fitur Mobile

- **Material Design 3** - Antarmuka modern dan intuitif yang dioptimalkan untuk mobile
- **Akses Berbasis Peran** - Aplikasi Siswa dan Guru dengan dasbor yang berbeda
- **Manajemen Izin** - Buat, ajukan, dan lacak surat di mana saja
- **Notifikasi Real-Time** - Notifikasi push untuk pembaruan status persetujuan
- **Dukungan Offline** - Fungsionalitas dasar tersedia tanpa internet
- **Autentikasi Biometrik** - Dukungan sidik jari dan pengenalan wajah
- **Pelacakan Surat** - Lacak surat yang diajukan dengan status real-time
- **Desain Responsif** - Tampilan sempurna di ponsel dan tablet

### Tumpukan Teknologi Mobile

| Komponen         | Teknologi                               |
| ---------------- | --------------------------------------- |
| **Platform**     | Android 8+ (minSdk 24)                  |
| **Bahasa**       | Kotlin 2.0                              |
| **Framework UI** | Android Jetpack + Material Design 3     |
| **Database**     | Room Database (persistensi lokal)       |
| **Jaringan**     | Retrofit 2 + OkHttp untuk panggilan API |
| **Auth**         | JWT dengan SharedPreferences            |
| **Pencatatan**   | HttpLoggingInterceptor (debug HTTP)     |

### Mulai Cepat (Mobile)

```bash
git clone https://github.com/e-letter/e-letter-android.git
cd e-letter-android
# Buka di Android Studio
# File > Sync Now > Run > Run 'app'
```

### Layar Utama Mobile

- Sambutan/Masuk - Autentikasi dengan pemilihan peran
- Dasbor Siswa - Beranda, buat surat, lihat surat, pelacakan
- Dasbor Guru - Beranda, tinjau permintaan, kelola persetujuan
- Formulir Izin - Buat surat dengan validasi formulir
- Riwayat Surat - Lihat semua surat yang diajukan
- Manajemen Profil - Profil dan pengaturan pengguna
- Notifikasi - Pembaruan persetujuan secara real-time

👉 [Lihat Proyek Mobile](https://github.com/e-letter/e-letter-android) | [Dokumentasi Lengkap](https://github.com/e-letter/e-letter-android#readme)

---

## 🔄 Alur Pengguna

### Alur Siswa

```text
Daftar/Masuk
     ↓
Pilih Jenis Izin
     ↓
Isi Formulir Izin
     ↓
Ajukan Permintaan
     ↓
Lacak Status Persetujuan
     ↓
Terima Persetujuan/Penolakan
```

**Tersedia di**: 🌐 Web | 🖥️ Desktop | 📱 Mobile

### Alur Guru

```text
Masuk
     ↓
Lihat Permintaan Tertunda
     ↓
Tinjau Informasi Siswa
     ↓
Setujui/Tolak/Minta Informasi
     ↓
Tambahkan Komentar & Tanda Tangan
     ↓
Beritahu Siswa Keputusan
```

**Tersedia di**: 🌐 Web | 🖥️ Desktop | 📱 Mobile

### Alur Administrator

```text
Masuk
     ↓
Kelola Pengguna
     ↓
Konfigurasi Alur Kerja
     ↓
Lihat Laporan Sistem
     ↓
Pantau Log Audit
     ↓
Kelola Pengaturan
```

**Tersedia di**: 🌐 Web | 🖥️ Desktop

---

## 🔐 Keamanan & Autentikasi

### Fitur Keamanan Umum

- **Kontrol Akses Berbasis Peran** - Manajemen izin yang terperinci
- **Penyimpanan Kata Sandi Aman** - Hashing bcrypt (Web/Backend), penyimpanan aman (Desktop/Mobile)
- **Manajemen Sesi** - Pembuatan dan pelacakan sesi yang aman
- **Pencatatan Audit** - Riwayat lengkap semua tindakan
- **Autentikasi Berbasis Token** - JWT untuk web, token sesi untuk desktop/mobile

### Keamanan Spesifik Platform

| Fitur                  | Web | Desktop | Mobile |
| ---------------------- | --- | ------- | ------ |
| Autentikasi JWT        | ✅  | ✅      | ✅     |
| Token Refresh          | ✅  | ✅      | -      |
| Penyimpanan Sesi Lokal | ✅  | ✅      | ✅     |
| HTTPS Hanya            | ✅  | -       | -      |
| Preferensi Terenkripsi | -   | -       | -      |
| Autentikasi Biometrik  | -   | -       | 🔜     |

### Hierarki Peran Pengguna

```text
ADMIN
├── Akses penuh sistem
├── Kelola pengguna & izin
└── Lihat semua laporan

KEPSEK (Kepala Sekolah)
├── Otoritas persetujuan akhir
├── Lihat statistik institusi
└── Ganti tahapan persetujuan

GURU_KESISWAAN (Guru Tata Tertib)
├── Tinjau permintaan siswa
├── Setujui/tolak surat
└── Tambahkan tanda tangan digital

GURU_MAPEL (Guru Mata Pelajaran)
├── Tinjau permintaan siswa di jadwalnya
├── Setujui/teruskan ke peran lebih tinggi
└── Kelola kegiatan kelas

SISWA (Siswa)
├── Ajukan permintaan izin
├── Lacak status permintaan
└── Lihat komentar persetujuan
```

### Sub-Peran Guru

Guru dapat memiliki beberapa sub-peran yang menentukan cakupan persetujuan:

| Peran          | Deskripsi               | Cakupan Persetujuan       |
| -------------- | ----------------------- | ------------------------- |
| **Wali Kelas** | Guru kelas              | Siswa kelasnya sendiri    |
| **Kapro**      | Kepala program keahlian | Siswa di jurusannya       |
| **Tatib**      | Guru tata tertib        | Semua siswa (tahap akhir) |
| **Guru Mapel** | Guru mata pelajaran     | Siswa di jadwalnya        |

---

## 📊 Perbandingan Fitur

| Fitur                   | Web | Desktop | Mobile   |
| ----------------------- | --- | ------- | -------- |
| Buat Surat Izin         | ✅  | ✅      | ✅       |
| Lacak Status Surat      | ✅  | ✅      | ✅       |
| Review/Persetujuan Guru | ✅  | ✅      | ✅       |
| Manajemen Admin         | ✅  | ✅      | -        |
| Pembaruan Real-Time     | ✅  | -       | ✅       |
| UI yang Indah           | ✅  | ✅      | ✅       |
| Dukungan Offline        | -   | ✅      | Sebagian |
| Dioptimalkan Mobile     | ✅  | -       | ✅       |
| Ekspor Laporan          | ✅  | ✅      | -        |
| Penyimpanan Database    | ✅  | ✅      | ✅       |

---

## 🗄️ Arsitektur Database

### Database Backend (MariaDB)

Digunakan bersama oleh klien Web dan Desktop melalui API Go. Terorganisir ke dalam **6 bagian logis**:

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

### Tabel Kunci

| Tabel                     | Tujuan                             | Bidang Kunci                                  |
| ------------------------- | ---------------------------------- | --------------------------------------------- |
| `users`                   | Akun pengguna                      | `id`, `username/email`, `role`, `status`      |
| `student_profiles`        | Data profil siswa                  | `user_id`, `student_code` (NISN), `signature` |
| `teacher_profiles`        | Data profil guru                   | `user_id`, `employee_code` (NIP), `signature` |
| `teacher_roles`           | Sub-peran guru per tahun ajaran    | `teacher_id`, `role_name`, `status`           |
| `requests`                | Permintaan surat izin              | `request_number`, `type_id`, `status`         |
| `request_approvals`       | Langkah alur persetujuan           | `request_id`, `step_no`, `approver_role`      |
| `approval_flow_templates` | Template alur persetujuan          | `type_id`, `step_no`, `approver_role`         |
| `jwt_tokens`              | Penyimpanan & pencabutan token JWT | `user_id`, `token_hash`, `is_revoked`         |

### Cache Klien-Sisi (SQLite — Desktop & Mobile)

| Tabel           | Tujuan                                       |
| --------------- | -------------------------------------------- |
| `local_letters` | Surat yang dibuat offline (menunggu sinkron) |
| `sync_queue`    | Antrian operasi untuk sinkronisasi tertunda  |
| `cached_users`  | Data referensi/master yang di-cache          |

---

## 🔌 Referensi API

### URL Dasar

```text
http://localhost:8080/api/v1
```

### Endpoint Autentikasi

| Endpoint        | Metode | Deskripsi            |
| --------------- | ------ | -------------------- |
| `/auth/login`   | POST   | Masuk pengguna       |
| `/auth/logout`  | POST   | Keluar pengguna      |
| `/auth/refresh` | POST   | Segarkan token akses |
| `/register`     | POST   | Daftar dengan token  |

### Endpoint Pengguna

| Endpoint        | Metode | Deskripsi       |
| --------------- | ------ | --------------- |
| `/user/profile` | GET    | Dapatkan profil |
| `/user/update`  | POST   | Perbarui profil |

### Endpoint Permintaan Izin

| Endpoint               | Metode | Deskripsi                |
| ---------------------- | ------ | ------------------------ |
| `/permission-requests` | GET    | Daftar permintaan izin   |
| `/permission-requests` | POST   | Buat permintaan izin     |
| `/permission-requests` | PUT    | Perbarui permintaan izin |
| `/permission-requests` | DELETE | Hapus permintaan izin    |
| `/approve`             | POST   | Setujui/tolak permintaan |

### Endpoint Surat

| Endpoint                       | Metode | Deskripsi                  |
| ------------------------------ | ------ | -------------------------- |
| `/letters/student/create`      | POST   | Buat surat siswa           |
| `/letters/teacher/create`      | POST   | Buat surat guru            |
| `/letters/student/izin-masuk`  | GET    | Dapatkan surat izin masuk  |
| `/letters/student/izin-keluar` | GET    | Dapatkan surat izin keluar |
| `/letters/student/dispensasi`  | GET    | Dapatkan surat dispensasi  |

### Kredensial Klien (Pengembangan)

| Peran     | Email      | Kata Sandi | Dasbor       |
| --------- | ---------- | ---------- | ------------ |
| **Siswa** | `123`      | `12345`    | Dasbor Siswa |
| **Guru**  | `G123`     | `12345`    | Dasbor Guru  |
| **Admin** | `admin123` | `12345`    | Panel Admin  |

---

## 🎨 Sistem Desain

Semua platform mengikuti bahasa desain modern yang konsisten dengan tema gradien dan efek glassmorphism.

### Palet Warna

| Jenis Izin         | Warna Utama | Gradien             |
| ------------------ | ----------- | ------------------- |
| Izin Masuk (Entry) | Ungu        | `#C471ED → #F64F59` |
| Izin Keluar (Exit) | Oranye      | `#FDC830 → #F37335` |
| Dispensasi         | Biru        | `#2193b0 → #6dd5ed` |

### Tipografi

| Konteks        | Web       | Desktop  | Mobile |
| -------------- | --------- | -------- | ------ |
| **Teks Tubuh** | Nunito    | System   | Roboto |
| **Judul**      | Quicksand | Segoe UI | Roboto |

### Pola Komponen

- **Kartu Interaktif** - Dapat dipilih dengan umpan balik visual
- **Animasi Halus** - Framer Motion (Web), WPF (Desktop), Material (Mobile)
- **Glassmorphism** - Efek blur latar belakang modern
- **Tata Letak Responsif** - Menyesuaikan semua ukuran layar

---

## 🛠️ Pengaturan Pengembangan

### Variabel Lingkungan (Web)

```env
# Basis Data
DB_HOST=localhost
DB_PORT=3306
DB_USER=eletter_user
DB_PASSWORD=your_password
DB_NAME=db_eletter

# Rahasia JWT
JWT_ACCESS_SECRET=your_access_secret
JWT_REFRESH_SECRET=your_refresh_secret

# Aplikasi
NODE_ENV=development
APP_ENV=development
APP_PORT=8080
```

### Variabel Lingkungan (Desktop — `App.config`)

```xml
<appSettings>
  <add key="ApiBaseUrl" value="http://localhost:8080/api/v1" />
  <add key="TimeoutSeconds" value="30" />
  <add key="EnableOfflineMode" value="true" />
  <add key="MaxRetryAttempts" value="3" />
</appSettings>
```

### Variabel Lingkungan (Backend Go — `.env`)

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

## 📱 Detail Pengaturan Mobile

### Prasyarat

- **Android Studio** (Arctic Fox atau lebih baru)
- **JDK 11** atau lebih baru
- **Android SDK** API Level 24 (minSdk 24) — Android 7.0+
- **Kotlin** 2.0.21
- **Server Backend** berjalan di `http://192.168.1.6:3000/`

### Konfigurasi URL Basis API

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

## 📞 Dukungan & Tautan

[🌐 Aplikasi Web](https://github.com/e-letter/e-letter-web) · [🖥️ Aplikasi Desktop](https://github.com/e-letter/e-letter-desktop) · [📱 Aplikasi Mobile](https://github.com/e-letter/e-letter-android)

[Laporkan Bug](https://github.com/e-letter/e-letter-web/issues) · [Minta Fitur](https://github.com/e-letter/e-letter-web/issues) · [Diskusi](https://github.com/e-letter/e-letter-web/discussions)

---

## 🙏 Ucapan Terima Kasih

### Dibangun Dengan

#### Web

- [Next.js](https://nextjs.org/) - Kerangka kerja React
- [Tailwind CSS](https://tailwindcss.com/) - Gaya
- [Framer Motion](https://www.framer.com/motion/) - Animasi
- [shadcn/ui](https://ui.shadcn.com/) - Komponen UI

#### Desktop

- [WPF-UI](https://github.com/lepoco/wpfui) - Kontrol WPF modern
- [Newtonsoft.Json](https://www.newtonsoft.com/json) - Serialisasi JSON
- [.NET Framework](https://dotnet.microsoft.com/) - Runtime

#### Mobile

- [Android Jetpack](https://developer.android.com/jetpack) - Kerangka kerja
- [Material Design 3](https://material.io/) - Sistem desain
- [Retrofit2](https://square.github.io/retrofit/) - Jaringan
- [Room Database](https://developer.android.com/jetpack/androidx/releases/room) - Persistensi

### Ucapan Khusus

- Komunitas open-source untuk alat dan pustaka luar biasa
- Semua kontributor dan pendukung proyek E-Letter

---

## 📄 Lisensi

**Lisensi Proprietary** - Seluruh Hak Dilindungi

Semua repositori E-Letter tersedia untuk:

- ✅ Keperluan edukasi dan pembelajaran
- ✅ Kontribusi melalui Pull Requests
- ✅ Penggunaan organisasi internal

Dilarang tanpa izin eksplisit:

- ❌ Redistribusi
- ❌ Membuat karya turunan
- ❌ Penggunaan komersial
- ❌ Menghapus pemberitahuan hak cipta

---

## 🏢 Struktur Organisasi

```text
E-Letter Organization
│
├── 🌐 e-letter-web (Situs Web)
│   ├── Next.js 16 + TypeScript
│   ├── Tailwind CSS 4 + shadcn/ui
│   ├── Framer Motion (Animasi)
│   ├── Database MariaDB 11.5
│   ├── Backend API Go 1.22 + Gin
│   └── Docker & Docker Compose
│
├── 🖥️ e-letter-desktop (Windows)
│   ├── .NET Framework 4.7.2 + WPF
│   ├── WPF-UI 4.2.1 (Fluent Design)
│   ├── Arsitektur MVVM
│   ├── Newtonsoft.Json 13.0.4
│   ├── SQLite (Cache Offline)
│   └── Notifikasi Toast Windows
│
└── 📱 e-letter-android (Mobile)
    ├── Android 14+ / Kotlin 2.0
    ├── Material Design 3
    ├── Kerangka Kerja Android Jetpack
    ├── Retrofit 2 + OkHttp
    ├── Room Database (rencana)
    └── Autentikasi Biometrik (rencana)
```

---

## 🚀 Rencana Masa Depan

- [ ] **Mode offline mobile** — Caching database Room untuk Android
- [ ] **Notifikasi push** — Integrasi Firebase Cloud Messaging
- [ ] **Autentikasi biometrik** — Pengenalan sidik jari & wajah (Mobile)
- [ ] **Lampiran foto/dokumen** — Integrasi kamera/galeri (Mobile)
- [ ] **Pembuatan & unduh PDF** — Ekspor surat yang disetujui
- [ ] **Dukungan multi-bahasa** — Internasionalisasi (i18n)
- [ ] **Tombol mode gelap** — Tombol saklar tema gelap/terang (Mobile)
- [ ] **Migrasi Jetpack Compose** — Toolkit UI modern untuk Android

---

Menyederhanakan manajemen surat izin sekolah di semua platform
