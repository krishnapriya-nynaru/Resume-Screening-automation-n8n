# 🤖 AI Resume Screener Workflow (n8n)

This is a complete automation workflow for resume screening using [n8n](https://n8n.io). The system extracts resumes from Gmail, parses and analyzes them using Google Gemini, matches them to a job description, and logs the evaluation results in Google Sheets.

## 📌 Key Features

- Gmail trigger for resume intake  
- File upload to Google Drive  
- Supports PDF, DOCX, and TXT  
- Extracts and analyzes resume content  
- LLM-powered screening using Gemini API  
- Stores structured results in Google Sheets  

---

## 🚀 Quick Start

1. 🖥️ [Install n8n on Ubuntu](./n8n-installation.md)
2. 🔐 [Set up Google Credentials](./google-credentials-setup.md)
3. 📥 Import `AI Resume analyser and screener.json` into n8n
4. ✅ Trigger workflow with a test email
5. 📊 Check Drive & Sheets for output

---

## 📷 Workflow Overview

![alt_text](https://github.com/krishnapriya-nynaru/Resume-Screening-automation-n8n/blob/main/resume-screening-automation-n8n/screenshots/intial_project.png?raw=true)

---

## 📄 Output Format

The final screening output contains structured analysis like this:

```json
{
  "candidate_strengths": [...],
  "candidate_weaknesses": [...],
  "risk_factor": { "score": "Low", "explanation": "..." },
  "reward_factor": { "score": "High", "explanation": "..." },
  "overall_fit_rating": 8,
  "justification_for_rating": "..."
}
```

## Technologies Used
- n8n (automation engine)
- Gmail API (trigger)
- Google Drive & Sheets (storage)
- Gemini via LangChain (LLM analysis)
