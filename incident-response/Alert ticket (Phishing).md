

| Ticket ID | Alert Message | Severity | Details | Ticket status |
| :---- | :---- | :---- | :---- | :---- |
| A-2703 | SERVER-MAIL Phishing attempt possible download of malware | Medium | The user may have opened a malicious email and attachments or clicked links. | **Escalated** |

| Ticket comments  |
| :---- |
| The phishing email was sent from an external source with the sender address Def Communications \<76tguyhh6tgftrt7tg.su\>. The IP address associated with this sender is 114.114.114.114. This email was sent to an employee on Wednesday, July 20, 2022, at 9:30:14 AM, prompting them to download an executable file (bfsvc.exe), which is highly suspicious. The file was also password-protected with the password "paradise10789", a common tactic to bypass automated malware detection. The email was received by hr@inergy.com (IP address: 176.157.125.93). This was intended to impersonate a job application process, convincing the recipient to open the file attachment, which may contain malware. Including a password for the file is another indication of a potential phishing attack, as this is a known method used to deliver malware.  |

### **Additional information**

**Known malicious file hash**: 54e6ea47eb04634d3e87fd7787e2136ccfbcc80ade34f246a12cf93bab527f6b

**Email**:  
From: Def Communications \<76tguyhh6tgftrt7tg.su\>  \<114.114.114.114\>  
Sent: Wednesday, July 20, 2022 09:30:14 AM  
To: \<hr@inergy.com\> \<176.157.125.93\>  
Subject: Re: Infrastructure Engineer role

Dear HR at Ingergy,

I am writing to express my interest in the engineer role posted on the website.

My resume and cover letter are attached. For privacy, the file is password protected. Use the password paradise10789 to open. 

Thank you,

Clyde West  
Attachment: filename="bfsvc.exe"
