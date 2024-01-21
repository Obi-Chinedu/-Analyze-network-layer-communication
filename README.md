# Analyze-network-layer-communication
I will analyze DNS and ICMP traffic in transit using data from a network protocol analyzer tool. I will identify which network protocol was utilized in assessment of the cybersecurity incident. 


# Cybersecurity Incident Report:

## Network Traffic Analysis

![image](https://github.com/Obi-Chinedu/-Analyze-network-layer-communication/assets/155754242/5a3f5c4d-96a0-4d3a-b8d3-2aa186da1d30)


#-- Part 1: Provide a summary of the problem found in the DNS and ICMP traffic log.
- The UDP protocol reveals that:
- This is based on the results of the network analysis, which show that the ICMP echo reply returned the error message:
- The port noted in the error message is used for:
- The most likely issue is:


#-- Part 2: Explain your analysis of the data and provide at least one cause of the incident.
- Time incident occurred:
- Explain how the IT team became aware of the incident:
- Explain the actions taken by the IT department to investigate the incident:
- Note key findings of the IT department's investigation (i.e., details related to the port affected, DNS server, etc.):
Note a likely cause of the incident:


  # Solution 
  ## Part 1: Summary of the Problem
  ***UDP Protocol Analysis:***
  -     Finding: The network analysis indicates the use of the UDP protocol for a domain name resolution request to the DNS server.
  - ![image](https://github.com/Obi-Chinedu/-Analyze-network-layer-communication/assets/155754242/943a38d0-9187-4076-af10-067f6e7fd757)
    ``In the initial outgoing request from your computer to the DNS server, a UDP packet is sent to request the IP address of yummyrecipesforme.com. The log includes timestamps indicating when events occurred, with the format HH:MM:SS.microseconds. Source and destination IP addresses are displayed, where the source is your computer's IP, and the destination is the DNS server's IP``

  ***ICMP Echo Reply Error:***
  -     Finding: The ICMP echo reply returns an error message, specifically "udp port 53 unreachable."
  - ![image](https://github.com/Obi-Chinedu/-Analyze-network-layer-communication/assets/155754242/4e3922aa-c7d7-4226-a117-5863b8bf9a64)
  ``The second  lines show an ICMP error message indicating that the ICMP packet was undeliverable to the port of the DNS server.``
    
  ***Port in the Error Message:***
  -     Finding: The error message mentions port 53, a well-known port for DNS service.
  ``The log specifies the protocol and port number (UDP port 53), signifying an attempt to resolve the domain name using the DNS server's address over port 53. The message "unreachable" indicates that the message did not reach the DNS server, implying that no service was listening on the DNS port.``
  
  ***Likely Issue:***
  -     Finding: The most likely issue is that the DNS resolution request over UDP to port 53 was unsuccessful, as indicated by the "unreachable" message. This suggests that no service was listening on the DNS port, impeding the retrieval of the IP address for yummyrecipesforme.com.


## Part 2: Analysis and Incident Details
***Time of Incident:***
Finding: The incident occurred at the timestamp indicated in the log, e.g., 13:24:32.192571.

***IT Team Awareness:***
Finding: I informed the IT team to be aware of the incident through routine monitoring of network traffic and analyzing logs.

***IT Department's Actions:***
Finding: I initiated an investigation into the incident, likely triggered by the detection of ICMP errors.

***Key Findings:***
Details: The investigation revealed repeated ICMP packets sent with the same delivery error. The port affected was UDP port 53, associated with DNS service.

***Likely Cause:***
Finding: The likely cause of the incident is that no service was listening on the DNS port (port 53), preventing the successful resolution of the domain name and impeding website access. This could be due to a misconfiguration, service unavailability, or a firewall issue.
