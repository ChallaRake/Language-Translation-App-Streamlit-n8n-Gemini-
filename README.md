# 🌐 Language Translation App (Streamlit + n8n + Gemini)

A lightweight, fast, and multilingual **AI-powered Translation Application** built using:

- **Streamlit** (Frontend UI)
- **n8n** (Backend Automation & Routing)
- **Google Gemini LLM** (Translation Engine)

This project allows users to enter text, select a target language, and instantly receive accurate translations powered by your n8n webhook workflow.

---

## 🚀 Features

- 🌍 Translate text into **30+ global languages**
- ⚡ Fast and efficient translation via n8n workflow
- 🤖 Powered by **Google Gemini LLM**
- 🧼 Clean, modern Streamlit interface
- 🔧 Configurable Webhook URL via environment variable
- 🛠 Debug mode with raw JSON response viewer
- 💾 Download translated text as a `.txt` file
- 🧠 Preserves formatting, emojis, line breaks, and tone

---

## 🧩 Project Architecture

### **1. Streamlit Frontend**
- File: `app.py`
- Handles user input, language selection, API calls, and displaying translations.

### **2. n8n Backend Workflow**
- File: `Lang_Translatn_Streamlit_Application using Webhook.json`
- Contains:
  - Webhook trigger
  - AI Agent (LangChain Agent)
  - Google Gemini Chat Model
- Sends back clean translated text.

---

## 🛠 Installation & Setup

### **1️⃣ Clone the Repository**
```bash
git clone https://github.com/your-username/language-translator
cd language-translator
```
### **2️⃣ Install Dependencies**
```bash
pip install -r requirements.txt
```

### **▶️ Run the Streamlit App**
```bash
streamlit run app.py
```

**Open in your browser:**
```arduino
http://localhost:8501
```

---

## 📡 API Communication
**Request sent from Streamlit → n8n**
```json
{
  "text": "Hello, how are you?",
  "target_language": "es",
  "language_name": "Spanish"
}
```
**Response returned by n8n**
```json
[
  {
    "output": "Hola, ¿cómo estás?"
  }
]
```
---

## 📝 Files in This Project
| File                                                      | Description                                                |
| --------------------------------------------------------- | ---------------------------------------------------------- |
| `app.py`                                                  | Streamlit frontend for translation UI                      |
| `Lang_Translatn_Streamlit_Application using Webhook.json` | n8n workflow containing Webhook + AI Agent + Gemini model  |
| `README.md`                                               | Documentation for your project                             |
| `requirements.txt`                                        | Python dependencies list                                   |

---

### 🔄 n8n Cloud or Self-Hosted
- Import workflow JSON
- Activate workflow
- Update Webhook URL if needed

---

## 📹 Demo Video

👉 **Watch the full workflow demo here:**  
### [*Language Translation App Automation*]()

---
<img width="1913" height="1047" alt="Screenshot 2025-11-25 210652" src="https://github.com/user-attachments/assets/e4c48361-8e1c-4348-81f1-bfcda7cf5518" />

