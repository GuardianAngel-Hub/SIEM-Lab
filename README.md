# 🚀 Elastic SIEM Lab

## 📌 Overview
This project sets up a **Security Information and Event Management (SIEM) Lab** using **Elastic Stack**. It collects security event logs from a **Kali Linux VM**, analyzes security incidents, and generates alerts.

## 🛠 Tools & Technologies Used
- **Elastic Stack (SIEM)**
- **Kibana** for log visualization
- **Elastic Agent** for log forwarding
- **Kali Linux** for security event generation
- **Nmap** for network scanning tests

## 📂 Project Structure
- **/Configs/** → Elastic SIEM configuration files & alert rules  
- **/Logs/** → Sample log files  
- **/Scripts/** → Automation scripts for testing SIEM  
- **/Screenshots/** → Kibana dashboards, queries, and alerts  

---

## 📖 Installation & Setup
### **1️⃣ Set Up an Elastic Account**
1. Sign up at [Elastic Cloud](https://cloud.elastic.co/registration)
2. Create a new **Elasticsearch** deployment
3. Wait for the setup to complete and get the **Cloud ID** & credentials

### **2️⃣ Install Kali Linux VM**
1. Download Kali Linux from [kali.org](https://www.kali.org/get-kali/)
2. Install it in **VirtualBox** or **VMware**
3. Set up networking (use **bridged mode** for better connectivity)

### **3️⃣ Install Elastic Agent in Kali**
1. Log in to **Elastic Cloud** → Go to **Integrations**
2. Search for **Elastic Defend** → Click **Install**
3. Copy the Linux installation command and run:
   ```bash
   sudo ./elastic-agent install --url=<your_elastic_url> --enrollment-token=<your_token>
4. Verify the agent is running:
   ```bash
   sudo systemctl status elastic-agent.service

  
### **4️⃣ Generate Security Events (Nmap Scan)
Run an Nmap scan to simulate an attack:
   ```bash
   sudo nmap -sS <target-ip>
-This should generate security events in Elastic SIEM.

---
🔍 Querying Security Events in Kibana
To search for Nmap scans in Kibana:

```bash
event.action: "nmap_scan" OR process.args: "sudo"

---
📊 Creating a Dashboard in Kibana
1. Open Kibana → Go to Dashboards
2. Click Create Dashboard → Add Visualization
3. Use an Area Chart to display event counts over time

---
🔔 Creating an Alert for Nmap Scans
1. Open Kibana → Go to Alerts & Rules
2. Click Create Rule → Use a Custom Query
3. Enter query:
```bash
event.action: "nmap_scan"

4. Set the rule to notify via email/Slack

📸 Screenshots

🎯 Next Steps
✅ Try generating different security events
✅ Experiment with failed SSH login attempts
✅ Add Windows logs to Elastic SIEM
✅ Improve detection rules

📫 Contact Me:
💼 LinkedIn: Your LinkedIn
📧 Email: your.email@example.com


---

## **Step 4: Upload Your Project to GitHub**
1. **Initialize Git** in your project folder:
   ```bash
   git init
   git add .
   git commit -m "Initial commit - SIEM Lab"


