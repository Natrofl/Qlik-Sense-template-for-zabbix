# Qlik-Sense-template-for-zabbix
### Description
Collects  QlikSense metrics (QRS, QPS, QRD, QSD, QES) from windows perfmon, also collects memory utilization for Qlik Sense processes such as engines, repository and etc
This template works only single-node sites installation.
### Requirements
Zabbix >=4.0 (need HTTP agent check)
Qlik Sense >= June 2019
### Installation
1. In QMC
Add virtual proxy witch the next parameters
* Descriptions - mon
* Prefix - mon
* Session inactivity timeout (minutes) - 30
* Session cookie header name - X-Qlik-Session-mon
* Anonymous access mode - Always anonymous user
* Server node - Central
* Additional response header - Cache-Control: no-cache
* Host white list: 127.0.0.1, your IP for internal network **(external domain or IP NOT SAFE!!!)**
* Click Apply

2. In Zabbix
* Import template via zabbix web-portal
* Assing on Qlik Sense host
* Change value of macro QPS_HOST to you Qlik Host internal IP.

