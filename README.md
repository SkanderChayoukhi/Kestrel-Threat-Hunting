# Kestrel-Threat-Hunting

## Résumé du projet

Le projet consiste à mettre en œuvre une solution de threat hunting (chasse aux menaces) en utilisant le langage Kestrel et le format STIX, dans le cadre de la sécurisation des réseaux 5G. Il s'agit d'un nouveau projet, ce qui signifie qu'il n'existe pas encore de ressources d'apprentissage supplémentaires, à l'exception des documentations officielles fournies. De plus, il n'y a pas d'exemples de scripts existants pour servir de guide ou de référence, ce qui implique que le développement des scripts a été fait sans modèle préétabli. Le but est de développer des scripts automatisés capables de détecter des menaces potentielles sur les réseaux, tout en assurant la virtualisation des environnements de test pour évaluer la performance des solutions développées.


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
#### * This scenario highlights key threats in 5G networks, including smishing campaigns, encrypted DNS-based C2 communication, and large-scale exploitation.
#### * Detection strategies emphasize behavioral analysis and anomaly detection while ensuring user privacy.
