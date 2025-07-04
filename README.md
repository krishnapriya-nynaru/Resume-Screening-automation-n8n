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

1. 🖥️ [Install n8n on Ubuntu](./resume-screening-automation-n8n/docs/n8n_installation_ubuntu.md)
2. 🔐 [Set up Google Credentials](./resume-screening-automation-n8n/docs/Google%20API%20Credentials%20Setup%20for%20n8n.md)
3. 🤖 [Set up Gemini API Key](./resume-screening-automation-n8n/docs/Get%20Your%20Google%20Gemini%20API%20Key.md)
4. 📥 Import `AI Resume analyser and screener.json` into n8n
5. ✅ Trigger workflow with a test email
6. 📊 Check Drive & Sheets for output

---

## 📷 Workflow Overview

![alt_text](https://github.com/krishnapriya-nynaru/Resume-Screening-automation-n8n/blob/main/resume-screening-automation-n8n/screenshots/workflow_n8n.png?raw=true)

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

## Contributing 
Contributions are welcome! To contribute to this project:
1. Fork the repository.
2. Create a new branch for your changes.
3. Make your changes and ensure the code passes all tests.
4. Submit a pull request with a detailed description of your changes.

## 🙏 Acknowledgements

- [**n8n**](https://n8n.io) – Open-source workflow automation platform powering this entire solution  
- [**Google Cloud Platform**](https://cloud.google.com) – OAuth, Gmail, Drive, Sheets, and Gemini AI APIs  
- [**LangChain**](https://www.langchain.com) – Framework for orchestrating LLM agents and tools  
- [**Google Gemini**](https://deepmind.google/technologies/gemini/) – LLM used for intelligent resume analysis  
- [**Ngrok**](https://ngrok.com) – Secure tunneling for local development and OAuth redirect handling  

---

✨ Whether you're streamlining recruitment or exploring intelligent automation, this workflow is your launchpad.  
Happy automating with n8n! ⚡

