## INCIDENT FINAL REPORT

### **Executive summary**

The organization experienced a security incident on August 28, 2024, at 7:20 p.m., PT, during which an individual could gain unauthorized access to customer personal identifiable information (PII) and financial information. Approximately 50,000 customer records were affected. The financial impact of the incident is estimated to be $100,000 in direct costs and potential loss of revenue. The incident is now closed, and a thorough investigation has been conducted.

### **Timeline**

At approximately 3:13 p.m., PT, on August  22, 2024, an employee received an email from an external email address. The email sender claimed that they had successfully stolen customer data. In exchange for not releasing the data to public forums, the sender requested a $25,000 cryptocurrency payment. The employee assumed the email was spam and deleted it.

On August  28, 2024, the same employee received another email from the same sender. This email included a sample of the stolen customer data and an increased payment demand of $50,000. 

The employee notified the security team on the same day, who began investigating the incident. Between August  28 and August  31, 2024, the security team concentrated on determining how the data was stolen and the extent of the theft.

### **Investigation**

The security team received the alert and traveled on-site to begin the investigation. 

The incident's root cause was identified as a vulnerability in the e-commerce web application. This vulnerability allowed the attacker to perform a forced browsing attack and access customer transaction data by modifying the order number included in the URL string of a purchase confirmation page. This vulnerability allowed the attacker to access customer purchase confirmation pages, exposing customer data, which the attacker then collected and exfiltrated.

After confirming the web application vulnerability, the security team analyzed the access logs. The logs indicated that the attacker accessed the information of thousands of purchase confirmation pages.

### **Response and remediation**

The organization collaborated with the public relations department to disclose the data breach to its customers. Additionally, the organization offered free identity protection services to customers affected by the incident. 

After the security team reviewed the associated web server logs, the cause of the attack was very clear. A single log source showed a high volume of sequentially listed customer orders.

### **Recommendations**

To prevent future recurrences, we are taking the following actions:

* Perform routine vulnerability scans and penetration testing.  
* Implement the following access control mechanisms:  
  * Implement an allow listing to allow access to a specified set of URLs and automatically block all requests outside this range.  
  * Ensure that only authenticated users are authorized access to content.

