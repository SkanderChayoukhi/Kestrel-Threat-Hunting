# Kestrel-Threat-Hunting

## Project Summary

The project involves implementing a threat hunting solution using the Kestrel language and the STIX format, within the context of securing 5G networks. This is a new project, meaning there are no additional learning resources available apart from the official documentation provided. Moreover, there are no existing script examples to serve as a guide or reference, which means the script development was carried out without any predefined models. The goal is to develop automated scripts capable of detecting potential threats on the networks, while ensuring the virtualization of testing environments to evaluate the performance of the solutions developed.


## 5G Attack Scenario: Multi-Stage Threat Overview
This document outlines the multi-stage threat scenario in a 5G network environment and the corresponding detection strategies.

### Stage 0: Reconnaissance
#### Objective
Harvest large pools of phone numbers for smishing campaigns.
#### Detection
 Monitor high-volume SMS targeting closely clustered number ranges.
### Stage 1: Infection (Smishing)
#### Method
Distribute phishing SMS to deliver malware (e.g., FluBot).
#### Detection
Analyze SMS activity for unusual patterns while preserving user privacy.
### Stage 2: Command & Control (C2)
#### Techniques
* DNS Tunneling/DGA: Use DNS to connect to C2 servers.
* Encrypted DNS (DoH/DNSSEC): Conceal traffic from telco monitoring.
#### Detection
Flag abnormal DNS patterns, bypassing telco DNS servers, or encrypted DNS behaviors.
### Stage 3: Exploitation
#### Objective
Use infected devices for botnets, DDoS attacks, or malware propagation.
#### Detection
Monitor coordinated high-volume data flows and behavioral anomalies.
### Notes
* ####  This scenario highlights key threats in 5G networks, including smishing campaigns, encrypted DNS-based C2 communication, and large-scale exploitation.
* ####  Detection strategies emphasize behavioral analysis and anomaly detection while ensuring user privacy.
