# SOC-Automation-with-Wazuh-Cortex-and-Shuffle
*Completed: November 1, 2025*

**description**

Tutorial by [MyDFIR](https://www.youtube.com/@MyDFIR).  
All implementation, exploration, and documentation performed independently as part of my cybersecurity learning journey.

- - - 

# Project Overview
description

## Tech Stack
| Tool & Technology | Purpose | Links |
|------------------|-----------------|-----------------|
| Wazuh       | SIEM/EDR platform for log collection, monitoring, and alerting | [https://wazuh.com/](https://wazuh.com/) |
| TheHive             | Incident response platform for case tracking | [https://strangebee.com/thehive/](https://strangebee.com/thehive/) |
| Shuffle             | SOAR platform for automated workflows  | [https://shuffler.io/](https://shuffler.io/) |
| Sysmon            | Endpoint telemtry for Windows  | [https://shuffler.io/](https://shuffler.io/) |
| Mimikatz           | Open-source credential-extracting tool used to simulate malicious activity | [https://github.com/ParrotSec/mimikatz](https://github.com/ParrotSec/mimikatz) |
| Windows 10 VM        | Endpoint environment to run Mimikatz and test Wazuh EDR detection | [https://www.vultr.com/](https://www.vultr.com/) |

- - -

# Architecture Diagram

<img width="1510" height="847" alt="Screenshot 2025-12-06 124107" src="https://github.com/user-attachments/assets/b7873087-d643-477c-a858-b45039c126df" />

1. Collect endpoint events of malicious behavior:
   
2. Wazuh Manager triggers alerts:
   
3. Shuffle receives Wazuh Alerts & sends responsive actions:

4. 

- - - 
# 🔢 Step-by-Step Walkthrough 🔢
## 1️⃣ Setup VM Lab Environment & Sysmon
To start, create a virtual machine, either using your own VM or a cloud-based service such as [Vultr](https://www.vultr.com/).  
For my lab, I used a [Virtualbox](https://www.virtualbox.org/) Windows 11 virtual machine.

1. To install a VirtualBox Windows 11 virtual machine, install the latest version from here: [https://www.virtualbox.org/](https://www.virtualbox.org/).  

2. Download a Windows 11 **.iso** file from [https://www.microsoft.com/en-us/software-download/windows11](https://www.microsoft.com/en-us/software-download/windows11).  

3. Add the **.iso** file to Virtualbox by navigating to New at the top of the screen, adding your .iso image, setting the version to Windows 11, and using all default settings.  
   - I recommend **8192 MB of base memory**, **2 processors**, and **80 GB** of hard disk storage space but it all depends on your setup.  
4. Startup your VM and follow the Microsoft setup. When it asks for product key, say you don't have one, and use Windows 11 Pro.  

5. Now let's setup Sysmon which can be installed from here: [https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon)

*Sysmon is a free tool created by Microsoft that provides detailed information about system activities on Windows by capturing and logging events. For this particular project, it will be used to flag our credential stealer called Mimikatz.*

6. From there, we will need a config to tell Sysmon what to ignore and what to log. Let's use **sysmonconfig.xml** from here: [https://raw.githubusercontent.com/olafhartong/sysmon-modular/refs/heads/master/sysmonconfig.xml](https://raw.githubusercontent.com/olafhartong/sysmon-modular/refs/heads/master/sysmonconfig.xml)
   - I saved it in my downloaded Sysmon directory.
  
7. In an **Administrative PowerShell** window, use ```cd``` to change directories to your Sysmon folder. Its likely located in your `downloads` folder. Then, run it using `\.Sysmon64.exe -i sysmonconfig.xml`.

**You now have a functional VirtualBox virtual machine with Sysmon installed!**

- - - 

## 2️⃣ Install Wazuh

- - - 

## 3️⃣ Configure Wazuh

- - - 

## 4️⃣ Install TheHive

- - - 

## 5️⃣ Configure TheHive

- - - 

## 6️⃣ Install Mimikatz on your VM

- - - 

## 7️⃣ Create a custom rule on Wazuh

- - - 

## 8️⃣ Create Shuffle SOAR Playbook

- - -

# Key Skills Demonstrated

- - - 

# Conclusion
