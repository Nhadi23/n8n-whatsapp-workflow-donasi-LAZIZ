# 🤖 WAHA – n8n AI Agent Workflow

Workflow ini adalah **WhatsApp Automation berbasis AI** menggunakan **n8n** yang terhubung dengan **WAHA (WhatsApp HTTP API)**.  
Workflow mampu menangani **pesan teks, gambar, dan audio**, memprosesnya dengan **AI Agent (LLM)**, serta melakukan **logging ke Google Sheets**.

Cocok untuk:
- Chatbot WhatsApp AI
- Customer service automation
- Voice-to-text bot
- Image analysis via WhatsApp
- Automation bisnis & SaaS WhatsApp

---

## ✨ Fitur Utama

- 📩 WhatsApp listener via **WAHA**
- 👁️ Auto *Seen Message*
- ⌨️ *Typing Indicator* (Start / Stop Typing)
- 🔀 Auto routing: **Text / Image / Audio**
- 🧠 AI Agent (Google Gemini / LLM lain)
- 🖼️ Image analysis
- 🎙️ Audio transcription
- 📊 Logging ke Google Sheets
- 🕒 Konversi timestamp ke **WIB**
- 🧩 Modular & scalable

---

## 🧱 Arsitektur Workflow


---

## 🧩 Node yang Digunakan

| Node | Fungsi |
|----|------|
| WAHA Trigger | Menerima event WhatsApp |
| Edit Fields | Normalisasi & timestamp |
| Send Seen | Menandai pesan terbaca |
| Wait | Delay agar natural |
| Switch | Routing text / image / audio |
| Aggregate | Gabungkan data pesan |
| HTTP Request (Image) | Ambil file gambar |
| Analyze Image | Analisis gambar via AI |
| HTTP Request (Audio) | Ambil file audio |
| Transcribe Recording | Audio → Text |
| AI Agent | Otak chatbot |
| Google Sheets | Logging data |
| Send Text Message | Kirim balasan |

---

## 🧩 Gambaran Singkat Workflow

Workflow ini berfungsi sebagai **WhatsApp AI Bot** dengan kemampuan:

- Menerima pesan WhatsApp (Text / Image / Audio)
- Menampilkan status *seen* dan *typing*
- Menganalisis pesan menggunakan AI Agent
- Transkripsi audio
- Analisis gambar
- Menyimpan log ke Google Sheets
- Mengirim balasan otomatis ke WhatsApp

---

## 🛠️ Persiapan Sebelum Import

Pastikan kamu sudah memiliki:

### 1️⃣ n8n (Wajib)
- Self-hosted (VPS / Docker / Coolify), atau
- n8n Cloud

### 2️⃣ WAHA (Wajib)
Digunakan sebagai WhatsApp Gateway

### 3️⃣ Akun Google (Opsional)
Untuk logging ke Google Sheets

### 4️⃣ API Key AI (Wajib)
Contoh:
- Google Gemini
- OpenAI
- LLM lain yang didukung n8n

### 5️⃣ Masukan Workflow
- buat workflow baru atau yang sudah lama
- copy paste dari code workflow.json dari github
- paste ke workflow anda
---
