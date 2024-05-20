# SIEM-Lab🚨
Looking to build a simple, free SIEM lab? Search no further. 

An integration of some very sophisticated open-source tools to work together in your production environment to automate generation of security alert, slack messaging, Incident response, triage, and overall asset monitoring.

Sit tight!
<h1>How It Works 💻</h1>
This project aims at securing assets in a production environment that communicates over the internet. It monitors assets and pull logs from them in real-time. 
Well, that of course doesn't tell the full story. 
Wazuh-agents are pushed to the endpoints and these 'wazuh-agents' is the responsible for pulling telemetry to Wazuh-manager.
Wazuh-manager is hosted locally but is connected to TheHive -a sophisticated case management system integrated with MISP and Shuffle -A platform which is responsible for alert forwarding via Slack and also for sending responsive actions to Wazuh-manager over the internet.

<h2>Requirements:</h2>
Wazuh-manger supports the following Operating systems:

|Amazon Linux 2| CentOS 7, 8|
|-------------| ------------|
|Red Hat Enterprise Linux 7, 8, 9| Ubuntu 16.04, 18.04, 20.04, 22.04 |

<h3>Minimum requirement</h3>

|Component|RAM (GB)| CPU (cores)|
|-------------|---|---|
|Wazuh server | 2 | 2 |

<h3>Recommended</h3>

|Component|RAM (GB)| CPU (cores)|
|-------------|---|---|
|Wazuh server | 4 | 8 |


| Linux| Windows|
|-------|-------|
