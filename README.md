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
PhishVision/
├── backend/                    # Backend API and ML components
│   ├── app.py                 # Main Flask application
│   ├── feature_extraction.py  # URL feature extraction module
│   ├── generate_dataset.py    # Dataset generation script
│   ├── train_model.py         # Model training script
│   ├── run_phishvision.py     # Automated setup script
│   ├── simple_test.py         # Basic testing script
│   ├── test_request.py        # API request testing
│   ├── test_system.py         # System integration tests
│   ├── phishing_dataset.csv   # Generated training dataset
│   ├── phishing_model.pkl     # Trained ML model
│   ├── README.md              # Backend documentation
│   ├── SYSTEM_STATUS.md       # System status and logs
│   └── venv/                  # Python virtual environment
│
├── extension/                  # Chrome extension files
│   ├── manifest.json          # Extension manifest
│   ├── popup.html             # Extension popup interface
│   ├── popup.js               # Popup functionality
│   ├── background.js          # Background script
│   ├── content.js             # Content script for page interaction
│   ├── style.css              # Extension styling
│   ├── icon.png               # Extension icon (128x128)
│   ├── icon_16.png            # Small icon (16x16)
│   ├── icon_48.png            # Medium icon (48x48)
│   └── create_icon.html       # Icon creation utility
│
├── dashboard/                  # Web dashboard (optional)
│   ├── index.html             # Dashboard interface
│   └── log.js                 # Logging functionality
│
├── utils/                      # Utility modules
│   ├── url_cleaner.py         # URL cleaning utilities
│   ├── whois_checker.py       # WHOIS lookup functionality
│   └── feature_list.txt       # Feature definitions
│
├── Screenshots/                # Documentation screenshots
│   ├── extension_view.png     # Extension interface
│   ├── phish_alert.png        # Phishing alert example
│   └── devtools_logs.png      # Developer tools logs
│
├── README.md                   # Main project documentation
├── INSTALLATION.md            # Installation guide
├── PROJECT_SUMMARY.md         # Project overview
├── FINAL_STATUS.md            # Final project status
├── requirements.txt           # Python dependencies
├── create_icon.py             # Icon generation script
├── test_backend.py            # Backend integration tests
├── test_phishing.html         # HTML test page
├── start_backend.bat          # Windows batch file to start backend
├── run_backend.sh             # Unix shell script to start backend
└── model.js                   # Additional model utilities
```

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
