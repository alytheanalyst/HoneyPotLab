# Project Title: Displaying Live Cyber Attacks on Microsoft Sentinel with a Honeypot  
For this project, I set up a Windows virtual machine (VM) in Azure to act as a honeypot, designed to attract and monitor RDP attacks in real time. I created a log repository in Azure to collect data from the VM and configured Microsoft Sentinel (a SIEM) to display a live map showing the geolocations of the attackers. To dig deeper, I used PowerShell scripts to extract the attackers’ IP addresses from the logs and sent them to an API to gather detailed location information. This data was then used to create custom logs with geographic details. The result was a system that not only tracked live attacks but also provided valuable insights into where they were coming from, making it a great example of using automation and visualization for threat monitoring.

## Utilities Used
- <b>ipgeolocation.io</b>
- <b>Microsoft Azure</b> 
  - <b>Microsoft Sentinel</b>
  - <b>Windows 10 VM</b>
  - <b>Log Analytics</b>
  - <b>PowerShell</b>
  - <b>Windows Event Viewer</b>


---

## Walk Through  

### Step 1: Creating the Virtual Machine (The Honeypot)  
**Description:**  
The first step in the process, after creating a free azure account, is the create and configure our Windows 10 virtual machine! It's important to give it an administrator user and password you'll remember.  

**Image:**  
![Creating The VM](images/windows10.png)

More importantly, we need to make sure our Windows machine is suceptible to attacks and basically free game to any hackers. Here's me configuring the security group to allow anything into the system.

![Creating The VM](images/networkgroup.png)

And here is an image of all the options I selected before creating the VM.

![Creating The VM](images/pressingcreate.png)


---

### Step 2: Configuring Log Analytics and Microsoft Sentinnel  
**Description:**  
The next step is to create our Log Analytics workspace. This will be used to ingest security event logs from the Windows VM. Later on, we will create a custom log that will give us geographic information to discover our hacker's locations in detail.
**Image:**  
![Step 2 Image](images/loganalytics.png)  

Then we want to head to Microsoft Defender so we can enable the ability to gather logs from the VM into the log analytics workspace. We want to collect all events.

![Step 2 Image](images/enablevmlogs.png)  

![Step 2 Image](images/enablevmlogs2.png)

Next, we want to actually connect our log analytics workspace to our honeypot.

![Step 2 Image](images/connecttovm.png)

Finally, we are going to connect Microsoft Sentinnel to our log analytics workspace. This is the SIEM we are going to use to visualize the attack data.

![Step 2 Image](images/connectsentinel.png)

---

### Step 3: [Step Title]  
**Description:**  
Explain what was achieved in this step, along with any challenges or key insights.  

**Image:**  
![Step 3 Image](path/to/image3.png)  

---

### Step 4: [Step Title]  
**Description:**  
Provide details of this step, focusing on the specific tasks completed.  

**Image:**  
![Step 4 Image](path/to/image4.png)  

---

### Step 5: [Step Title]  
**Description:**  
Write a description of this step, emphasizing its role in the project’s overall workflow.  

**Image:**  
![Step 5 Image](path/to/image5.png)  

---

### Step 6: [Step Title]  
**Description:**  
Outline what was achieved in this step and its contribution to the final goal.  

**Image:**  
![Step 6 Image](path/to/image6.png)  

---

### Step 7: [Step Title]  
**Description:**  
Explain the focus of this step and any specific tools, methods, or configurations used.  

**Image:**  
![Step 7 Image](path/to/image7.png)  

---

### Step 8: [Step Title]  
**Description:**  
Highlight the objectives of this step and describe how they were met.  

**Image:**  
![Step 8 Image](path/to/image8.png)  

---

### Step 9: [Step Title]  
**Description:**  
Provide an in-depth overview of this step and its importance to the project’s success.  

**Image:**  
![Step 9 Image](path/to/image9.png)  

---

### Step 10: [Step Title]  
**Description:**  
Summarize this final step, emphasizing its completion and any key takeaways.  

**Image:**  
![Step 10 Image](path/to/image10.png)  

---

## Conclusion  
Wrap up your project by summarizing its purpose, key outcomes, and future potential. Highlight any challenges overcome and what you learned during the process.  

## Takeaways  
Include steps for anyone interested in running or contributing to your project. Provide setup instructions, prerequisites, and how to reproduce your results
