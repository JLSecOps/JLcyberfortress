# **Cybersecurity Incident Report:** 

# **Network Traffic Analysis**

| Part 1: Provide a summary of the problem found in the DNS and ICMP  traffic log.  |  |
| :---- | ----- |
| The UDP protocol reveals that the DNS service was affected due to the error message "udp port 53 unreachable." This message indicates that the UDP packets sent to the DNS server on port 53 were not delivered successfully because no service was listening on the receiving DNS port. The DNS server was not responding to requests due to the absence of a listening service on port 53, which caused the "destination port unreachable" error.  |  |
|  |  |

| Part 2: Explain your analysis of the data and provide at least one cause of the incident. |
| :---- |
| The incident occurred at 1:24 p.m., 32.192571 seconds. The IT team became aware of the incident when clients reported that they were unable to access the website www.yummyrecipesforme.com and encountered the error message "destination port unreachable."  The IT department used a network analyzer tool, tcpdump, to capture and analyze the network traffic. They attempted to access the website and observed the same error, confirming the issue. The analysis showed that UDP packets sent to the DNS server resulted in ICMP error messages indicating the unreachability of port 53\. The DNS server's IP address was 203.0.113.2. UDP packets were sent from the source IP address 192.51.100.15 to the destination IP address 203.0.113.2 on port 53\. ICMP error messages indicated that port 53 was unreachable. The DNS service was not functioning correctly, preventing the domain name from being converted to an IP address. The likely cause of the incident was that the DNS service on the server was not active or was misconfigured, resulting in the "udp port 53 unreachable" error. |

**Step 3: Summary of the Problem Found in the tcpdump Log**

**Summary of the tcpdump Log Analysis**:

* The tcpdump log analysis revealed that the network traffic involved the DNS protocol, which uses UDP, and the ICMP protocol.  
* The primary issue identified was the repeated ICMP error message "udp port 53 unreachable," indicating that UDP packets sent to the DNS server on port 53 were not being processed.

**Details from the Log:**

* The log showed initial outgoing UDP requests from the client’s IP address (192.51.100.15) to the DNS server (203.0.113.2) for resolving the domain name yummyrecipesforme.com.  
* ICMP responses were returned from the DNS server, indicating that the destination port (port 53\) was unreachable.

**Interpretation of the Issues:**

* The ICMP error messages suggest that the DNS server was not listening on port 53, which is essential for processing DNS queries. This resulted in the inability to resolve the domain name, making the website inaccessible.

**Record in Part One of the Cybersecurity Incident Report:**

* The network traffic utilized the UDP protocol for DNS queries and the ICMP protocol for error messaging.  
* The issue was identified as the DNS server not responding on port 53, causing the "destination port unreachable" error.

**Step 4: Analysis of the Data and Solution Implementation**

**Explanation of the Data Analysis:**

* The error messages appeared because the DNS server was not accepting UDP packets on port 53, necessary for DNS resolution.  
* The protocols involved revealed a communication breakdown between the client and the DNS server due to the unresponsive DNS service.

**When the Problem was First Reported:**

* The issue was first reported when clients could not access the website and received the error message "destination port unreachable."

**Scenario, Events, and Symptoms:**

* Clients reported access issues to the website yummyrecipesforme.com.  
* The symptom was the error message indicating that the destination port was unreachable, preventing DNS resolution.

**Current Status of the Issue**:

* The issue persists as the DNS server is still not responding to queries on port 53\.

**Information Discovered During Investigation:**

* The DNS server (203.0.113.2) is not listening on port 53, leading to the ICMP error messages.  
* UDP packets are not being processed due to the inactive DNS service.

**Next Steps in Troubleshooting and Resolving the Issue:**

1. Verify the DNS server configuration to ensure the DNS service is active and listening on port 53\.  
2. Restart the DNS service if necessary to re-establish proper communication.  
3. Monitor the network traffic post-resolution to confirm normal operation.

**Suspected Root Cause of the Problem:**

* The root cause is likely a misconfiguration or failure of the server's DNS service, which prevents it from listening on the required port.

**Record in Part Two of the Cybersecurity Incident Report:**

* Detailed the analysis of the error messages and identified the DNS service issue as the root cause.  
* Proposed solutions include verifying and restarting the DNS service to resolve the issue.
