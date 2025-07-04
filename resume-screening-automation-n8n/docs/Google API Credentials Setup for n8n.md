# 🔐 Google API Credentials Setup for n8n

This guide will walk you through connecting Google Drive, Google Sheets, and Gmail to **n8n** using OAuth credentials.

---

## ✅ Step 1: Prepare in n8n

1. Open your **n8n UI** in the browser.
2. Double-click any Google node (e.g., Google Drive, Google Sheets, or Gmail).
3. Under **Credential to connect with**, click **Create New**.
4. You'll need the **Client ID** and **Client Secret** from Google Cloud Console.

![alt_text](https://github.com/krishnapriya-nynaru/Resume-Screening-automation-n8n/blob/main/resume-screening-automation-n8n/screenshots/n8n_credentials.png?raw=true)


---

## 🔗 Step 2: Go to Google Cloud Console

> Link: [https://console.cloud.google.com/](https://console.cloud.google.com/)

1. Create a new **Google Cloud Project** (or use an existing one).
2. Click into your project.

![alt_text](https://github.com/krishnapriya-nynaru/Resume-Screening-automation-n8n/blob/main/resume-screening-automation-n8n/screenshots/intial_project.png?raw=true)

---

## 📦 Step 3: Enable Required APIs

Go to: **APIs & Services → Enable APIs and Services**

Search for and enable the following:

- ✅ Google Drive API  
- ✅ Gmail API  
- ✅ Google Sheets API  

![alt_text](https://github.com/krishnapriya-nynaru/Resume-Screening-automation-n8n/blob/main/resume-screening-automation-n8n/screenshots/enable_services.png?raw=true)


---

## 🔑 Step 4: Create OAuth Credentials

Go to: **APIs & Services → Credentials → Create Credentials**

1. Click **Create Credentials** → Select **OAuth Client ID**
2. Choose **Application Type**: _Web Application_
3. Give it a **name** (e.g., `n8n OAuth`)
4. Under **Authorized Redirect URIs**, copy it from n8n and paste here:
   - In n8n, copy the **OAuth Redirect URL**
   - Paste that URL here in Google Console

![alt_text](https://github.com/krishnapriya-nynaru/Resume-Screening-automation-n8n/blob/main/resume-screening-automation-n8n/screenshots/create_credentials.png?raw=true)

![alt_text](https://github.com/krishnapriya-nynaru/Resume-Screening-automation-n8n/blob/main/resume-screening-automation-n8n/screenshots/create_OAuth.png?raw=true)


5. Click **Create**
6. Download the JSON — you'll need the **Client ID** and **Client Secret**

---

## 🧩 Step 5: Fill OAuth Details in n8n

1. Go back to n8n → Paste the **Client ID** and **Client Secret** into the credential settings
2. Click **Sign in with Google**
3. Complete the OAuth login

Repeat this step for:

- **Google Sheets node**
- **Gmail node**

---

## 🎨 Step 6: Configure OAuth Consent Screen

Go to: **OAuth Consent Screen → Edit App**

1. Under **App Branding**, fill:
   - App name
   - User support email
   - Developer email

2. Under **Authorized Domains**, add your **ngrok domain**:
   - Open terminal:
     ```bash
     ngrok http 5678
     ```
   - Copy the generated HTTPS domain (e.g., `https://xxxxxxxxxxxx.ngrok-free.app`)
   - Paste only the domain part into **Authorized Domains**
---

## 🚀 Step 7: Publish App

1. In the **OAuth Consent Screen**, scroll to **Publishing Status**
2. Click **Publish App**

Your OAuth app is now live and usable in n8n!

---

## 🔁 Final Step: Connect and Test

- In n8n, go back to your Google node
- Click **Sign In with Google**
- Grant permissions

You are now ready to use:

- 📂 Google Drive
- 📄 Google Sheets
- 📩 Gmail

in your **automated workflows**! 🎉

---


