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

  



<!--<h1>JWipe - Disk Sanitization</h1>

 ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)

<h2>Description</h2>
Project consists of a simple PowerShell script that walks the user through "zeroing out" (wiping) any drives that are connected to the system. The utility allows you to select the target disk and choose the number of passes that are performed. The PowerShell script will configure a diskpart script file based on the user's selections and then launch Diskpart to perform the disk sanitization.
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Diskpart</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<h2>Program walk-through:</h2>

<p align="center">
Launch the utility: <br/>
<img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Select the disk:  <br/>
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Enter the number of passes: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm your selection:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
