# Website-certificates-monitoring-template-for-Zabbix
Easily monitor certificates on multiple websites with use of Zabbix agent 2 built-in functionality. Tested on Zabbix 6.4.4.
## Why two versions?
There are two versions of the template. They only vary in way they get targeted websites information in JSON format. In website_certificate_sender.yaml is the JSON sent using zabbix_sender. In website_certificate_macro.yaml is the JSON stored in macro and is set within Zabbix web interface for easier usage.
## How to use
1. Create JSON in following format
  - ```{"data":[{"{#CMNAME}":"<common name>", "{#PORT}":"<port number>", "{#IPADDR}":"<ip address>"}]} ```
  - example of filled JSON
    - ```
      {"data":[{ "{#CMNAME}":"google.com", "{#PORT}":"443", "{#IPADDR}":"142.251.36.110"}, { "{#CMNAME}":"seznam.cz", "{#PORT}":"443", "{#IPADDR}":"77.75.77.222"}]}
      ```
2. Create new macro (only macro version)
  - administration > macros > add
  - set macro name to `{$WEBSITE_CERTIFICATE_TARGETS_LIST}`
  - as value set the JSON
3. Import desired template
4. Assign it to host
5. Use zabbix_sender to send JSON (only sender version)
  - install zabbix_sender on your system
  - send item with key `targets.list` and value of JSON
