# SIEM-Lab
Looking to build a simple, free SIEM lab? Search no further. 

This project is a net-integration of some very sophisticated open-source tools to work together in other to automate generation of security alert, real-time monitoring of endpoints, Incident response, triage, and Slack messaging. Sit tight!
<h1>How It Works</h1>
This project aims at securing assets (windows computers where used in this project) in a production environment that communicates over the internet. It monitors these endpoints and pull logs from them in real-time. 
Well, that of course doesn't tell the full story. 
Wazuh-agents are pushed to the windows clients and this 'wazuh-agent' is the program responsible for pulling telemetry to Wazuh-manager.
The wazuh-manager is hosted locally but is also connected to TheHive (A sophisticated case management system integrated with MISP) and Shuffle (A platform which is responsible for alert forwarding via Slack and also for sending responsive actions to Wazuh-manager).
