# Windows SOC Lab

## Objective

In this cyber home lab, I set up a basic SOC in Microsoft Azure from scratch. I was able to create a virtual machine and open it to the internet as a honeypot, then forward the recorded logs to a central repository. I then integrated Microsoft Sentinel to analyze real-world attack data, including failed login attempts and visualizing attack sources in real time.

This project was great for practicing log analysis, threat detection, and SOC operations in a real-world cloud environment.

### Skills Learned

- Advanced understanding of SIEM concepts and practical application.
- Proficiency in analyzing and interpreting network logs.
- Ability to recognize attack signatures and patterns.
- Enhanced knowledge of security vulnerabilities.

### Tools Used

- Microsoft Azure to create a virtual machine as a honeypot.
- Security Information and Event Management (SIEM) system for log ingestion and analysis. (Microsoft Sentinel)


## Steps

1) Created a Virtual Machine to use as a honeypot, which is connected to a resource group and virtual network. I then opened the firewall of the network security group to allow all traffic. 

    <img width="1440" alt="image" src="https://github.com/user-attachments/assets/75e3963f-d635-4cf0-90e8-d7784a439cd1" />
   <img width="1440" alt="image" src="https://github.com/user-attachments/assets/0033b934-b981-4cb4-809a-830f42f3c83f" />

2) Connected my VM to Windows remotely using Remote Desktop and disabled the firewall.

   <img width="1440" alt="image" src="https://github.com/user-attachments/assets/9da858f4-6a6c-41e4-9a40-184c921532b0" />

3) Pinged my VM's public IP address to assure attackers could reach it.

   <img width="560" alt="image" src="https://github.com/user-attachments/assets/8a4531ab-0329-4624-baa7-a8cad1320f9f" />

4) Created a Log Repository then connected it to my VM to forward the logs to it.

   <img width="1440" alt="image" src="https://github.com/user-attachments/assets/d32f8f5b-79bc-44c8-8dad-dae39f29fde1" />

5) Installed Windows Security Events as my SIEM.

   <img width="1440" alt="image" src="https://github.com/user-attachments/assets/c3544a30-65ee-4448-a3c9-e0c678d4ae11" />
   <img width="1440" alt="image" src="https://github.com/user-attachments/assets/9e03286c-e0d6-4d7c-9847-1f10fde95779" />

6) Using a spreadsheet of different IP address ranges and where they are in the world, I uploaded the Geolocation data to the SIEM in order to pin point the attackers.
    <img width="1440" alt="image" src="https://github.com/user-attachments/assets/13e9afc7-c045-4b53-9847-d5720535e36a" />
    <img width="1440" alt="image" src="https://github.com/user-attachments/assets/53314c4c-c41c-41e9-a304-b89ad99e1fcd" />

7) I used queries to analyze the logs, narrowing it down to failed login attempts and allowing me to see where the attempts were happening from and at what time.
   <img width="1440" alt="image" src="https://github.com/user-attachments/assets/abf6b87b-3131-42ef-b21d-facafc426761" />

8) I finally created an attack map in Microsoft Sentinel Workbooks to use as a visual to pin point exacty where the attacks are coming from using the below queries:  
    <img width="1440" alt="image" src="https://github.com/user-attachments/assets/103abab8-802d-4c4b-a066-ef4d181d7cfa" />
    <img width="1440" alt="image" src="https://github.com/user-attachments/assets/e04c28fd-f323-4b10-845c-e31e4fb37a40" />


