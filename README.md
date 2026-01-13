# SIGAPIT Mobile (Flutter)

SIGAPIT Mobile adalah aplikasi pengaduan masalah informasi dan teknologi (IT) berbasis **Flutter** yang terintegrasi
dengan backend **Laravel** (SIGAPIT Web).  
Aplikasi ini ditujukan untuk **role Pengadu**, sedangkan Admin dan Kepala Dinas
menggunakan versi web.

---

## 🚀 Fitur Utama
- Login 
- Dashboard pengadu
- List & detail pengaduan
- Buat pengaduan + upload gambar
- Attachment private 
- Preview fullscreen + zoom
- Light & Dark Mode 
- Bottom Navigation

---

## 🧱 Arsitektur Sistem

Kalau kampus tidak minta label:

```md
```mermaid
flowchart TB
    Flutter[Flutter Mobile App]
    Laravel[Laravel Backend API]
    DB[MySQL Database]

    Flutter --> Laravel
    Laravel --> DB

