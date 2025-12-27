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

## 🔌 Setup WAHA

### 1️⃣ Jalankan WAHA (Docker)

```bash
docker run -d \
  --name waha \
  -p 3000:3000 \
  -e WHATSAPP_DEFAULT_ENGINE=WEBJS \
  -e WHATSAPP_API_KEY=your_api_key \
  devlikeapro/waha
Webhook URL:
https://your-n8n-domain/webhook/waha
