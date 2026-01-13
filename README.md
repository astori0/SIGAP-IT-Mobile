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

```mermaid
flowchart TB
    A[Flutter Mobile App]
    B[Laravel Backend API]
    C[MySQL Database]

    A -->|REST API JSON| B
    B --> C
```
---

## 🔐 Integrasi dengan SIGAPIT Web

Aplikasi mobile **TIDAK berdiri sendiri**, tetapi menggunakan **backend yang sama**
dengan aplikasi web SIGAPIT.

### 🔹 Backend yang digunakan
- Laravel 10
- Laravel Sanctum (Authentication)
- Role-based access control

### 🔹 Pembagian Role
| Role | Platform |
|-----|----------|
| Pengadu | Mobile (Flutter) |
| Admin | Web |
| Kepala Dinas | Web |

---

## 🔄 Alur Integrasi Mobile ↔ Web

### 1️⃣ Autentikasi
- Mobile login via `POST /api/login`
- Token disimpan menggunakan Sanctum
- Token dikirim via header:
