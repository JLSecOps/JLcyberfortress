### **Data leak worksheet**

---

**Incident summary:** During a meeting, a sales manager shared access to a folder of internal-only documents with their team. The folder contained files associated with a new product that had not been publicly announced and customer analytics and promotional materials. After the meeting, the manager did not revoke access to the internal folder but warned the team to wait for approval before sharing the promotional materials with others.

During a video call with a business partner, a sales team member forgot the warning from their manager. The sales representative intended to share a link to the promotional materials so that the business partner could circulate them to their customers. However, the sales representative accidentally shared a link to the internal folder instead. Later, the business partner posted the link on their company's social media page, assuming that it was the promotional materials.

| Control | Least privilege |  |  |
| :---- | :---- | ----- | ----- |
| **Issue(s)** | *What factors contributed to the information leak? The factors that led to the data leak, including the manager's oversight and the representative's mistake, highlight the need for proactive preventive measures. It's crucial that we increase awareness and vigilance in our data security practices to prevent such incidents in the future.* |  |  |
| **Review** | *What does NIST SP 800-53: AC-6 address? NIST SP 800-53: AC-6 addresses the principle of least privilege, which entails providing users only the minimum access necessary to complete their tasks. It aims to prevent users from operating at higher privilege levels than required, reducing the risk of data leaks and unauthorized access.* |  |  |
| **Recommendation(s)** | *How might the principle of least privilege be improved at the company? Restrict access to sensitive resources based on user role to ensure only authorized personnel can access critical information. Automatically revoke access to the information after a set period to minimize the chances of unnecessarily prolonged access.*  |  |  |
| **Justification** | *How might these improvements address the issues? Implementing these enhancements will ensure that sensitive information is only accessible to those who truly need it, reducing the chances of accidental sharing. Automatic revocation of access after a set period will help prevent unauthorized access to information that is no longer necessary for certain users to have.* |  |  |

### **Security plan snapshot**

The NIST Cybersecurity Framework (CSF) organizes information using a hierarchical, tree-like structure. From left to right, it describes a broad security function and then becomes more specific as it branches out to a category, subcategory, and individual security controls.

| Function | Category | Subcategory | Reference(s) |
| :---- | :---- | :---- | :---- |
| **Protect** | PR.DS: *Data security* | PR.DS-5: *Protections against data leaks.* | NIST SP 800-53: AC-6 |

In this example, the manufacturer's implemented controls to protect against data leaks are defined in NIST SP 800-53, a set of guidelines for securing the privacy of information systems.

**Note:** References are commonly hyperlinked to the guidelines or regulations they relate to. This makes it easy to learn more about how a particular control should be implemented. Multiple links to different sources are common in the references columns.

### **NIST SP 800-53: AC-6**

NIST developed SP 800-53 to provide businesses with a customizable information privacy plan. It's a comprehensive resource that describes a wide range of control categories. Each control provides a few key pieces of information:

* **Control:** A definition of the security control.  
* **Discussion:** A description of how the control should be implemented.  
* **Control enhancements:** A list of suggestions to improve the effectiveness of the control.

| AC-6 | Least Privilege |
| :---- | :---- |
|  | Control: Only the minimal access and authorization required to complete a task or function should be provided to users. |
|  | Discussion: Processes, user accounts, and roles should be enforced as necessary to achieve least privilege. The intention is to prevent a user from operating at privilege levels higher than what is necessary to accomplish business objectives. |
|  | Control enhancements: Restrict access to sensitive resources based on user role. Automatically revoke access to information after a period of time. Keep activity logs of provisioned user accounts. Regularly audit user privileges. |

**Note:** In the category of access controls, SP 800-53 lists least privilege sixth, i.e. AC-6.  
