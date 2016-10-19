# 20 October 2016
This repository contains the scripts i run on my home automation server. It consists of:  
1. Scripts to monitor critical IP addresses on the network.

Credit to Rohit for the monitorip.sh script

# Installation:
```
git clone https://github.com/sfilinto/home_automation_script_v3_monitoringscripts.git
cd home_automation_script_v3_monitoringscripts
chmod a+x install_script
sudo ./install_script
```

# Post Installation:

Add the below line to the crontab (crontab -e)  to have the IP addresses monitored
```
@reboot /usr/local/bin/ipmonitor/monitorip.sh -u /usr/local/bin/ipmonitor/action_16up -e 192.168.0.16
@reboot /usr/local/bin/ipmonitor/monitorip.sh -u /usr/local/bin/ipmonitor/action_17up -e 192.168.0.17
@reboot /usr/local/bin/ipmonitor/monitorip.sh -u /usr/local/bin/ipmonitor/action_21up -e 192.168.0.21
```

