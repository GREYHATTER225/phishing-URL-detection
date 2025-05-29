 Phishing URL Detection using Machine Learning

This project is a practical implementation of a **phishing URL detection system** using machine learning. The system classifies URLs as *legitimate* or *phishing* by analyzing multiple features extracted from the URLs.

→🎓 Built as part of my BTech 2nd Year Practical — Cybersecurity Module.


→🚀 Features

- 🔍 **URL Feature Extraction**: Extracts over 20 handcrafted features from each URL.
- 🧠 **Machine Learning Model**: Pre-trained model used for real-time prediction.
- 🌐 **Web Interface**: User-friendly web app (Flask) for easy input and output.
- 📦 **Modular Code**: Easy to maintain and expand for future improvements


→📁 phishing-URL-detection/

├── README.md                  # 📘 Project description
├── requirements.txt           # 📦 Python dependencies
├── main.py                    # 🔁 Command line execution
├── app.py                     # 🌐 Flask web application
├── model/
│   └── model.pkl              # 🎯 Pre-trained ML model
├── utils/
│   └── helper.py              # 🛠️ Helper functions (if needed)
├── features/
│   ├── featureExtractor.py    # 🔍 Feature extraction pipeline
│   └── extractorFunctions.py  # 🔎 Functions for URL analysis
├── templates/
│   └── index.html             # 🧾 HTML for the web UI
├── static/
│   ├── css/
│   │   └── style.css          # 🎨 Optional styling
│   └── img/
│       └── screenshot1.png    # 📸 Store screenshots here
├── screenshots/
│   ├── web_demo.png           # 📸 Screenshot of the web app
│   └── cli_demo.png           # 📸 Screenshot of CLI mode
└── .gitignore                 # 🧽 Ignore unnecessary files (e.g. __pycache__)



→🧠 How It Works

1. User submits a URL via the web app or CLI.
2. The URL is passed to `featureExtractor.py`, which analyzes characteristics like:
   - Length of the URL
   - Presence of special characters (e.g., `@`, `-`)
   - Use of HTTPS
   - Number of subdomains
   - URL redirection
3. Extracted features are sent to a pre-trained **Random Forest Classifier**.
4. The classifier returns a prediction:
   - `0` → Legitimate
   - `1` → Phishing

→🛠️ How to Run It
    Setup (First Time Only)

     ```
git clone https://github.com/GREYHATTER225/phishing-URL-detection.git
cd phishing-URL-detection
pip install -r requirements.txt
```
💻 Launch CLI Mode

python main.py


🌐 Launch Web App

python app.py
# Then open http://127.0.0.1:5000/ in your browser


Training Data: The model was trained on a labeled dataset of ~10,000 URLs (phishing and legitimate).

Model Used: Random Forest Classifier (95% accuracy during testing).

📉Performance Metrics:

Accuracy: 95%

Precision: 93%

Recall: 96%

F1 Score: 94%





📸 Screenshots





🌐Web Interface

Sample output for phishing and legit URLs

Terminal view of CLI version


🔐 Disclaimer

This tool is for educational and research purposes only. Do not use it for malicious activities.




⭐ Future Improvements (MAY BE FOR SURE 😊)

Improve model accuracy using transformer-based URL embedding.

Add live URL scanning via VirusTotal API.

Add database to track blacklisted URLs over time.

🦾 Keep Learning

> Built with 💻, 
☕ and a lot of
 Ctrl+C / Ctrl+V 😅 ( just kidding )

 AND FINNALLY 

"In the world of lies... I’ll be the truth." —  Uzumaki
