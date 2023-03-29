# Sysdig Windows Prometheus Bundle
The Sysdig Windows Prometheus Bundle is a comprehensive package that installs and configures a [Prometheus Agent](https://prometheus.io/blog/2021/11/16/agent/) and the [Windows Exporter](https://github.com/prometheus-community/windows_exporter) allowing you to send metrics to your Sysdig Monitor account with ease. 

<p align="center"><img src="./media/installer-1.png" > </img></p>

## Key features: 
* User-friendly visual installation wizard
* Interactive enabling of [a vast variety of collectors](https://github.com/prometheus-community/windows_exporter#collectors)
* Prometheus Agent and Windows Exporter run as Windows services
* Metrics enriched with Windows Domain and Instance host name for easy identification in Sysdig Monitor

## Getting Started
To begin monitoring your Windows machines, follow these steps: 
1. Download the binary installer from the latest release of this project
2. Run the installer in your windows machine
3. Configure the [Sysdig region](https://docs.sysdig.com/en/docs/administration/saas-regions-and-ip-ranges/#sysdig-platform-regions) and your Sysdig API token in the wizard
4. Select the collectors that you want to enable to produce metrics

## Automated installation
You can automate the installation of the Sysdig Windows Prometheus Bundle across multiple machines using the command line or PowerShell.

Use the following command as an example: 
```
msiexec /i windows_exporter-0.0.1-x64.msi COMPUTER_NAME=PC-DEMO 
ENABLED_COLLECTORS=cpu,os 
SYSDIG_URL="https://collector-staging.sysdigcloud.com/prometheus/remote/write" 
SYSDIG_TOKEN="yyyyyyy-zzzz-zzzz-zzzz-xxxxxxxx" /qn
```

This command will install the Sysdig Windows Prometheus Bundle with the specified settings, making it easy to deploy across your infrastructure.