# Syntax Errors - Red-Flag Browser Extension

## 🔥 Overview
**Red-Flag** is a powerful browser extension designed to combat misinformation and ensure the integrity of online content. This extension employs advanced AI technologies to detect **deepfake videos**, **check facts in real-time**, and **analyze sentiment for bias detection**.

It is based on the **Red-Flag Extension** concept and improves upon it by integrating the **GenConViT** model for deepfake detection, **Google's Fact Checker API** for misinformation verification, and **RoBERTa sentiment analysis** for bias detection.

---

## 🚀 Features

### 🟢 Deepfake Detection
- Leverages the **GenConViT model** (a hybrid convolutional-transformer architecture from Hugging Face).
- Analyzes videos to determine **authenticity and detect deepfakes**.
- Works on embedded videos from various platforms.

### 🟡 Misinformation Detection
- Uses **Google's Fact Checker API** to verify the **authenticity of news and articles**.
- Classifies claims into:
  - ✅ **TRUE** (supported by sources)
  - ❌ **FALSE** (contradicted by sources)
  - ⚠️ **MISLEADING** (partially true, exaggerated, or lacking full context)
  - 🤷 **NO EVIDENCE** (no related news articles available)

### 🔴 Bias Detection
- Utilizes **Twitter's RoBERTa sentiment analysis model**.
- Detects bias in articles by analyzing sentiment.
- Highlights potential bias in the **headline and body text** of a webpage.

---

## 📁 Project Structure

Syntax_Errors_DLW/ │── src/ │ ├── backend/ │ │ ├── text_process/ # Misinformation & Bias Detection │ │ │ ├── api.py # FastAPI server │ │ │ ├── text_analysis.py # Text classification logic │ │ ├── video_process/ # Deepfake Detection │ │ │ ├── GenConViT/ # Model implementation │ │ │ ├── videoEndpoints.py # API endpoints for video analysis │ ├── frontend/
│ │ ├── images/ # Extension icons and assets
│ │ ├── content.css # Styles for the extension
│ │ ├── content.js # Script to interact with web pages
│ │ ├── popup.html # UI for the extension popup
│ │ ├── popup.js # Controls popup behavior
│ │ ├── manifest.json # Browser extension manifest

yaml
Copy
Edit

---

## 🛠️ Installation

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/Pyder3/Syntax_Errors_DLW.git


cd Syntax_Errors_DLW


uvicorn src.backend.text_process.api:app --reload
---bash 


4️⃣ Load the Extension in Browser
Open Chrome and go to chrome://extensions/.
Enable Developer Mode (top right corner).
Click "Load Unpacked" and select the src/frontend folder.
The Red-Flag extension should now be active!


🔥 How It Works
✅ Misinformation Detection (Text Processing API)
Extracts text from the webpage.
Calls the Fact Checker API to verify claims.
Displays results inside the extension popup.
🎥 Deepfake Detection (Video Processing API)
Extracts video from a webpage.
Uses GenConViT to check if the video is a deepfake.
Displays results in the extension popup.
📊 Bias Detection (Sentiment Analysis)
Analyzes headline & body text for bias.
Uses RoBERTa sentiment model to classify bias.
Provides a confidence score inside the popup.


🏗️ Tech Stack
Frontend: HTML, CSS, JavaScript (Chrome Extension API)
Backend: Python, FastAPI
Machine Learning: Hugging Face (GenConViT, RoBERTa)
APIs: Google's Fact Checker API


🤝 Contributing
Want to improve Red-Flag? Follow these steps:
Fork the repository
Create a new branch (git checkout -b feature-name)
Make your changes
Commit and push (git commit -m "Added feature X" && git push origin feature-name)
Submit a Pull Request (PR)



📜 License
This project is licensed under the MIT License.

📬 Contact
For questions or suggestions, open an issue on GitHub:
🔗 GitHub Repository

pgsql
Copy
Edit

This is already formatted as markdown (`README.md` file). You can simply **copy and paste** it int
