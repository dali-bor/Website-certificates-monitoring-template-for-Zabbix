# How to use website_certificate_macro.yaml
1. Create JSON in the following format
  - ```{"data":[{"{#CMNAME}":"<common name>", "{#PORT}":"<port number>", "{#IPADDR}":"<ip address>"}]} ```
  - example of JSON
    - ```
      {"data":[{ "{#CMNAME}":"google.com", "{#PORT}":"443", "{#IPADDR}":"142.251.36.110"}, { "{#CMNAME}":"seznam.cz", "{#PORT}":"443", "{#IPADDR}":"77.75.77.222"}]}
      ```
2. Create a new macro
  - administration > macros > add
  - set macro name to `{$WEBSITE_CERTIFICATE_TARGETS_LIST}`
  - as a value set JSON
3. Import a `website_certificate_macro.yaml` template into Zabbix
4. Assign it to host
