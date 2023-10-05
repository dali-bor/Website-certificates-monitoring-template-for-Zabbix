# How to use website_certificate_macro.yaml
1. Create JSON in the following format
  - ```{"data":[{"{#CMNAME}":"<common name>", "{#PORT}":"<port number>", "{#IPADDR}":"<ip address>"}]} ```
  - example of JSON
    - ```
      {"data":[{ "{#CMNAME}":"google.com", "{#PORT}":"443", "{#IPADDR}":"142.251.36.110"}, { "{#CMNAME}":"seznam.cz", "{#PORT}":"443", "{#IPADDR}":"77.75.77.222"}]}
      ```
2. Import a `website_certificate_macro.yaml` template into Zabbix
3. Give the macro `{$WEBSITE_CERTIFICATE_TARGETS_LIST}` value of the JSON
4. Assign the template to host
