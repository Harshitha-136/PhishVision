# 🛡️ PhishVision

**PhishVision** is a real-time Chrome extension that detects phishing websites using AI-powered analysis. It alerts users instantly with Chrome notifications and ensures all processing happens locally for privacy and performance.

## 🚀 Features
- 🔍 Real-time phishing detection
- 🤖 AI-powered backend (Flask + Python)
- 🔔 Instant Chrome alerts
- 🔒 100% local processing
- ⚙️ Lightweight & fast

## 🧠 How It Works
1. Chrome extension monitors URLs.
2. Sends URL to Flask backend via API.
3. Backend analyzes the URL for suspicious patterns.
4. If phishing is detected, the user is notified instantly.

## 🖼️ Demo

### 🔗 Visiting a suspicious site
![Verifying with Cloudflare](https://raw.githubusercontent.com/yourusername/PhishVision/main/Screenshot%202025-07-05%20180724.png)

### 🧪 AI analysis via DevTools logs
![Console output](https://raw.githubusercontent.com/yourusername/PhishVision/main/Screenshot%202025-07-05%20183634.png)

### 🔌 Chrome extension UI
![Extension installed](https://raw.githubusercontent.com/yourusername/PhishVision/main/Screenshot%202025-07-05%20183751.png)

## 📦 Project Structure
![image](https://github.com/user-attachments/assets/eda9a0e4-f911-45eb-8a32-00569f358058)
## ⚙️ Setup

### 1. Install Python dependencies
```bash
pip install -r requirements.txt
2. Start Flask server
cd backend
python app.py
3. Load Chrome Extension
Go to chrome://extensions/

Enable Developer Mode

Click “Load unpacked” and select the extension/ folder

📡 API
POST /predict → { url: "https://example.com" }
Returns: phishing/safe + confidence level
