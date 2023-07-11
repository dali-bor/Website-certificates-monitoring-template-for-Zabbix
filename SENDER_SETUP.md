# How to use website_certificate_sender.yaml
1. Create JSON in the following format
  - ```{"data":[{"{#CMNAME}":"<common name>", "{#PORT}":"<port number>", "{#IPADDR}":"<ip address>"}]} ```
  - example of JSON
    - ```
      {"data":[{ "{#CMNAME}":"google.com", "{#PORT}":"443", "{#IPADDR}":"142.251.36.110"}, { "{#CMNAME}":"seznam.cz", "{#PORT}":"443", "{#IPADDR}":"77.75.77.222"}]}
      ```
3. Import a `website_certificate_sender.yaml` template into Zabbix
4. Assign it to a host
5. Use zabbix_sender to send JSON
  - install zabbix_sender on your system
  - send an item with a `targets.list` key and a value of JSON
