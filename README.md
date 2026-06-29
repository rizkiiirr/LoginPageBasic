# Arsitektur Direktori Sistem Manajemen Pengujian Tanah

Struktur direktori ini mengikuti pola *Modern Laravel Data Architecture* dengan pemisahan logika bisnis yang ketat menggunakan pola *Action-Domain-Responder* dan *Observer pattern*.

```text
.
├── app/
│   ├── Actions/                # Logika bisnis 
│   │   └── UploadCertificate/  # Modul unggah sertifikat
│   ├── Http/
│   │   ├── Controllers/        # Pengendali alur permintaan (Controller)
│   │   ├── Middleware/         # Proteksi rute (Auth, Role-based)
│   │   └── Requests/           # Validasi data (FormRequest)
│   ├── Models/                 # Entitas data (Eloquent Models)
│   ├── Observers/              # Event-driven logic (Notifikasi)
│   └── Policies/               # Otorisasi akses 
├── database/
│   ├── migrations/             # Skema basis data
│   └── seeders/                # Data awal (Role, Akun Uji)
├── docs/                       # Dokumentasi teknis dan operasional
├── resources/
│   └── views/                  # Antarmuka pengguna 
├── routes/
│   └── web.php                 # Definisi rute aplikasi
├── storage/                    # Penyimpanan berkas (MinIO/Local)
└── tests/
    ├── Feature/                # Pengujian fungsional (TDD)
   
