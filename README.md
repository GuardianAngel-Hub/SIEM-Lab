







-------------------------------------------------------
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
