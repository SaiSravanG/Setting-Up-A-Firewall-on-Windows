# Setting-Up-A-Firewall-on-Windows
Setting up a Windows Firewall and Hovering over the Existing Rules and adding new ones and testing them to block inbound traffic

Tools Used:
-> Windows Defender Firewall
-> Command Prompt
-> netsh

To Setup and Use a Firewall press Windows + R and type : wf.msc

<img width="392" height="200" alt="image" src="https://github.com/user-attachments/assets/44bd0763-e1d1-449a-877b-f22e83873ae0" />

This opens the Windows Defender Firewall with Advanced Security.

To Look at Existing Rules Click on the "Inbound Rules" within the Windows Firewall and note down the current rules set for each application.

<img width="1042" height="780" alt="image" src="https://github.com/user-attachments/assets/9432158f-05f3-42f1-9762-b27e286bb36a" />

To Add a New Rule go to Inbound Rules -> New Rule

<img width="352" height="69" alt="image" src="https://github.com/user-attachments/assets/5bbbcc57-e1d2-40cb-b2f5-aa41f0f4741d" />

->Then Select Port -> TCP -> Specific local ports: 23
<img width="717" height="573" alt="image" src="https://github.com/user-attachments/assets/cd2043fa-f9d2-4ebc-aca7-8bfd0fdedac7" />

<img width="710" height="581" alt="image" src="https://github.com/user-attachments/assets/72706b40-d43d-4684-ae70-f7ef50927a5f" />

->Choose Block the connection

<img width="707" height="570" alt="image" src="https://github.com/user-attachments/assets/b49f6ad3-11b0-408c-b599-38d2f0fe17d7" />

->Name it Block Telnet Port 23

<img width="705" height="569" alt="image" src="https://github.com/user-attachments/assets/e7a94fb0-a134-47e4-b942-5ba74a3a1fe8" />

<img width="353" height="247" alt="image" src="https://github.com/user-attachments/assets/a77b35ea-5261-4915-beb8-6efe1ea6ae9f" />

Explanation: Here We are adding a new rule which is for temporary purposes where we are blocking port number 23 connected via tcp and it is named by Telnet Communications.

To Verify if the port is blocked 

Go to Command Prompt and type in "netsh advfirewall firewall show rule name=all"

<img width="752" height="391" alt="image" src="https://github.com/user-attachments/assets/b1259a9c-7895-482c-98a3-8683da63bf04" />

Firewall Filters Traffic: examines incoming and outgoing network packets and deciding whether to allow or block them based on rules

-> A data packet arrives at the computer and if the packet matches the rule then it is permitted or else its blocked 
