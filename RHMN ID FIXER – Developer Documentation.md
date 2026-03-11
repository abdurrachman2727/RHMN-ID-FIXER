RHMN ID FIXER adalah platform berbasis WPA yang dikombinasikan dengan Firebase Backend untuk menyediakan layanan digital seperti:

Unlock SIM All Carrier

Unblock IMEI

Device Information Tools

IMEI Scanner

Online Service Order

Sistem ini menggunakan pendekatan serverless architecture dengan Firebase sebagai backend utama.

🏗 System Architecture
Client Browser
      │
      ▼
 Template (Frontend)
      │
      ▼
JavaScript Application
      │
 ┌───────────────┬───────────────┬───────────────┐
 ▼               ▼               ▼
Firebase Auth   Firestore DB   Firebase Storage
      │               │               │
      └───────────────┴───────────────┘
                      │
                      ▼
                 Service Data
🧰 Technology Stack
Frontend

HTML5

CSS3

JavaScript ES6

Template Engine

Backend

Firebase Authentication

Firebase Firestore

Firebase Storage

Libraries
OCR Engine
Tesseract.js

Digunakan untuk membaca teks dari gambar.

Contoh penggunaan:

Image → Scan → Extract Text → Detect IMEI
Icons
Font Awesome

Digunakan untuk UI icon seperti:

Menu

Button

Notification

Feature icons

📂 Project Structure

Contoh struktur proyek:

rhmn-id-fixer/
│
├── template.xml
│
├── assets
│   ├── css
│   │   └── style.css
│   │
│   ├── js
│   │   ├── app.js
│   │   ├── firebase.js
│   │   └── ocr.js
│   │
│   └── images
│
├── components
│   ├── header
│   ├── footer
│   └── sidebar
│
└── documentation
    └── developer.md
🔐 Authentication System

Sistem login menggunakan:

Firebase Authentication

Metode login yang didukung:

Email / Password

Google Sign In

Flow login:

User Login
   │
   ▼
Firebase Auth
   │
   ▼
User UID Generated
   │
   ▼
Database Access Granted
🗄 Database Structure

Database menggunakan:

Firebase Firestore
Collection: Users
users
 ├ uid
 ├ email
 ├ role
 ├ created_at
 └ status
Collection: Orders
orders
 ├ order_id
 ├ user_id
 ├ service_type
 ├ imei
 ├ device_model
 ├ status
 ├ payment_status
 └ created_at
Collection: Scan Results
scan_results
 ├ id
 ├ image_url
 ├ extracted_text
 ├ detected_imei
 └ created_at
📤 File Upload System

Upload menggunakan:

Firebase Storage

Digunakan untuk:

screenshot device

bukti pembayaran

image scan IMEI

Flow upload:

User Upload Image
       │
       ▼
Firebase Storage
       │
       ▼
URL File
       │
       ▼
Saved to Firestore
🔎 OCR Scanner System

Engine yang digunakan:

Tesseract.js

Proses:

User Upload Image
      │
      ▼
OCR Processing
      │
      ▼
Text Extraction
      │
      ▼
IMEI Detection

Contoh output:

IMEI: 352099001761481
📦 Features
1️⃣ IMEI Scanner

Fungsi:

membaca imei dari gambar

extract data device

Teknologi:

Tesseract OCR
2️⃣ Unlock SIM Service

Mendukung berbagai carrier:

AT&T

Verizon

Spectrum

Dish Boost

Cricket

Tracfone

3️⃣ Unblock IMEI Service

Fungsi:

mengaktifkan kembali IMEI terblokir

kompatibel dengan berbagai negara

4️⃣ Service Order System

User dapat:

submit order
upload bukti
track status
5️⃣  Article System

Karena berbasis wpa, sistem juga menyediakan:

artikel teknologi

panduan unlock sim

tutorial device repair

🔒 Security Recommendations

Agar sistem lebih aman:

Firestore Rules

Gunakan rule seperti:

allow read, write: if request.auth != null;
API Key Protection

Jangan expose API key di frontend tanpa restriction.

Anti Spam

Tambahkan:

Google reCAPTCHA
⚙ Installation Guide
Step 1


Theme → Backup/Restore → Upload XML
Step 2

Setup Firebase Project

Firebase Console

Buat:

Firestore

Authentication

Storage

Step 3

Masukkan konfigurasi Firebase

Contoh:

const firebaseConfig = {
  apiKey: "XXXX",
  authDomain: "XXXX",
  projectId: "XXXX",
  storageBucket: "XXXX",
};
📊 Roadmap

Future development:

Version 2.0

Admin dashboard

Payment gateway

API unlock automation

Version 3.0

Mobile app

AI device detection

automatic IMEI parsing

🤝 Contributing

Jika ingin berkontribusi:

Fork repository

Create branch

Submit pull request

📜 License

Project ini digunakan untuk:

RHMN ID FIXER Service Platform

All rights reserved.

🌐 Official Website
https://www.rhmnidfixers.my.id
