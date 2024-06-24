# SIEM-Lab🚨
Looking to build a sophisticated, free SIEM lab with SOAR integrations? Search no further. 

An integration of some of the most powerful open-source tools to work together in your production environment to automate the generation of security alerts, slack messaging, active incident response, triage, and overall asset monitoring.

Sit tight!
<h1>How It Works 💻</h1>
This project aims at securing assets in a production environment that communicates over the internet. It monitors assets and pull logs from them in real-time. 

Well, that of course doesn't tell the full story. 

Wazuh-agents are pushed to the endpoints and these 'wazuh-agents' are responsible for pulling telemetry to Wazuh-manager.

Wazuh-manager is hosted locally and is connected to TheHive -a versatile case management system, inbuilt in it is MISP- a threat intelligence platform (CTI) and Cortex -a platform for active response and intelligence gathering.

![image](https://github.com/EmmyNwani/SIEM-Lab/assets/114263866/8f095928-ab2a-42d6-90b0-caa0bc89d9ef)

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

The fastest way to run this installation is by using the installation assistant. 
In your Ubuntu Terminal, enter:

`curl -sO https://packages.wazuh.com/4.8/wazuh-install.sh && sudo bash ./wazuh-install.sh -a`

Or, you can [Check out the wazuh documentation](https://documentation.wazuh.com/current/quickstart.html) page.

# TheHive
For thehive to run optimally and efficiently, some other programs will be have to be installed along with it. For this installation, we will use docker. 
TheHive has [Cortex](https://docs.thehive-project.org/cortex/) and [MISP](https://www.misp-project.org/) integrated into it by default.

Use this [docker-compose](https://github.com/EmmyNwani/SIEM-Lab/blob/main/docker-compose.yml) file to install thehive and its dependent applications.

Create a docker-compose.yml file and paste the contents of the [dockerfile](https://github.com/EmmyNwani/SIEM-Lab/blob/main/docker-compose.yml) into it.

Navigate to the path where the docker-compose.yml file is located and run a `docker-compose up -d` command to run the installation on docker.

After you are done installing the [docker-compose](https://github.com/EmmyNwani/SIEM-Lab/blob/main/docker-compose.yml) file, you will need to set them up seperately via their web interfaces. 
Navigate to the web interface of [Cortex](https://docs.thehive-project.org/cortex/) and [MISP](https://www.misp-project.org/) to get your MISP and Cortex servers up and ready to be integrated with thehive by creating accounts and organizations on the platforms.

<h2>Requirements:</h2>

|RAM| Storage|
|---|--------|
|4GB|80GB|

# Connecting TheHive and Wazuh 

For thehive and wazuh to work across board, two things must be done.

First, the custom python thive `custom-w2thive` integration must be downloaded and configured appropriately.
Secondly, wazuh's `ossec.conf` file will be edited and theHive's API and IP added to the `ossec.conf` file.
Follow the steps in [wazuh's page](https://wazuh.com/blog/using-wazuh-and-thehive-for-threat-protection-and-incident-response/) and be sure to follow the same indentation in the `ossec.conf` file. 

For reference, The [w2thive](https://github.com/EmmyNwani/SIEM-Lab/blob/main/custom-w2thive) and [w2thive.py](https://github.com/EmmyNwani/SIEM-Lab/blob/main/custom-w2thive.py) files can be found in this piece.

# Reference and Further Research
To learn more about Wazuh, thehive, Cortex, MISP or to troubleshoot your installation, visit the following pages.

https://thehive-project.org/# 

https://docs.strangebee.com/

https://github.com/thehive-project/Cortex/

https://documentation.wazuh.com/current/quickstart.html

https://wazuh.com/blog/using-wazuh-and-thehive-for-threat-protection-and-incident-response/
