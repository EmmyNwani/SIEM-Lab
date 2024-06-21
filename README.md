# SIEM-Lab🚨
Looking to build a sophisticated, free SIEM lab with SOAR integrations? Search no further. 

An integration of some of the most powerful open-source tools to work together in your production environment to automate generation of security alert, slack messaging, Incident response, triage, and overall asset monitoring.

Sit tight!
<h1>How It Works 💻</h1>
This project aims at securing assets in a production environment that communicates over the internet. It monitors assets and pull logs from them in real-time. 
Well, that of course doesn't tell the full story. 
Wazuh-agents are pushed to the endpoints and these 'wazuh-agents' are responsible for pulling telemetry to Wazuh-manager.
Wazuh-manager is hosted locally and is connected to TheHive -a versatile case management system, inbuilt in it is MISP- a threat intelligence platform (CTI) and Cortex -a platform for active response and intelligence gathering.

![Github Project drawio](https://github.com/EmmyNwani/SIEM-Lab/assets/114263866/fa7ccf50-aa30-445d-92dc-1f0bdc8ecac7)

# Wazuh
<h2>Requirements:</h2>
Wazuh-manger supports the following Operating systems:

|Amazon Linux 2| CentOS 7, 8|
|-------------| ------------|
|Red Hat Enterprise Linux 7, 8, 9| Ubuntu 16.04, 18.04, 20.04, 22.04 |

Wazuh-agent supports the following Operating systems:

|Linux |Windows|macOS|Solaris|AIX|HP-UX|
|------|-------|-----|-------|---|-----|
<h3>Minimum requirement</h3>

|Component|RAM | CPU (cores)|
|-------------|-------|---|
|Wazuh server | 2 GB  | 2 |
|Wazuh agent  | 35 MB | 1 |


<h3>Recommended</h3>

|Component|RAM| CPU (cores)|
|-------------|---|---|
|Wazuh server | 4 GB | 8 |
|Wazuh agent  | >35 MB | 1 |

# TheHive
