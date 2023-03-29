# Sysdig Windows Prometheus Bundle
The Sysdig Windows Prometheus Bundle is a binary file that installs in your Windows based machine a [Prometheus Agent](https://prometheus.io/blog/2021/11/16/agent/) and the [Windows Exporter](https://github.com/prometheus-community/windows_exporter), and configures them to send the metrics to your Sysdig Monitor account. 

<p align="center"><img src="./media/installer-1.png" > </img></p>

Main features: 
* Easy visual installation wizard
* Enable interactively [a vast variety of collectors](https://github.com/prometheus-community/windows_exporter#collectors)
* Prometheus Agent and Windows Exporter as Windows services
* Enriched metrics with Windows Domain and Instance host name to identify each machine metrics in Sysdig Monitor

# Getting Started
To start monitoring your Windows machines, follow these steps: 
1. Download the binary installer from the latest release of this project
2. Execute the installer in your windows machine
3. Configure the [Sysdig region](https://docs.sysdig.com/en/docs/administration/saas-regions-and-ip-ranges/#sysdig-platform-regions) and your Sysdig API token in the wizard
4. Choose the collectors that you want to enable to produce metrics

## Automating the installation
You can also use the command line or PowerShell to automate the installation of the Sysdig Windows Prometheus Bundle in multiple machines.

To do this, you can use the following command as example: 
```
msiexec /i windows_exporter-0.0.1-x64.msi COMPUTER_NAME=PC-DEMO 
ENABLED_COLLECTORS=cpu,os 
SYSDIG_URL="https://collector-staging.sysdigcloud.com/prometheus/remote/write" 
SYSDIG_TOKEN="yyyyyyy-zzzz-zzzz-zzzz-xxxxxxxx" /qn
```
