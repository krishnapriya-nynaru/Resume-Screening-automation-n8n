# 🛠️ n8n Installation Guide (Ubuntu Server)

This guide helps you install `n8n` — a powerful open-source workflow automation tool — on a desktop, VM, or cloud VPS running Ubuntu.

---

## ✅ Prerequisites

Before you begin, make sure you have:

- 💻 Desktop PC, Virtual Machine, or Cloud VPS
- 🐧 Ubuntu Server Installed (20.04+ recommended)
- 🔐 SSH Access
- 🔧 Root or sudo privileges

---

## 📦 Installation Steps

### 1. Update the System

```bash
sudo apt update && sudo apt upgrade -y
```
### 2. Install Node.js and npm
- Go to: https://deb.nodesource.com/
- Find the latest LTS version setup script (e.g., 20.x)
- Run the following:
```bash
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo bash -
sudo apt-get install -y nodejs
```
### 3. Verify Node.js and npm Installation
```bash
node --version
npm --version
```
### 4. Update npm to Latest Stable Version
```bash
sudo npm install -g npm@10.9.2
```
### 5. Install n8n Globally
```bash
sudo npm install -g n8n
```
### 6. Start n8n
```bash
n8n
```
**Note:** n8n will now run locally. By default, it uses port 5678.

🌐 Open it in your browser at: http://<your-server-ip>:5678

**Optional:** 

Use a Real Database: By default, n8n stores data in SQLite.

For production-grade deployments, it's highly recommended to switch to PostgreSQL.


