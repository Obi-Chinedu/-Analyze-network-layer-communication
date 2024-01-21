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
  *UDP Protocol Analysis:**
  -     Finding: The network analysis indicates the use of the UDP protocol for a domain name resolution request to the DNS server.
  - ICMP Echo Reply Error:
  -     Finding: The ICMP echo reply returns an error message, specifically "udp port 53 unreachable."
  - Port in the Error Message:
  -     Finding: The error message mentions port 53, a well-known port for DNS service.
  - Likely Issue:
  -     Finding: The most likely issue is that the DNS resolution request over UDP to port 53 was unsuccessful, as indicated by the "unreachable" message. This suggests that no service was listening on the DNS port, impeding the retrieval of the IP address for yummyrecipesforme.com.
