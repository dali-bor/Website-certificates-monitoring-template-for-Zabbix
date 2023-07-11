# Website-certificates-monitoring-template-for-Zabbix
<img width="1487" alt="Screenshot 2023-07-11 at 16 09 45" src="https://github.com/dali-bor/Website-certificates-monitoring-template-for-Zabbix/assets/139234961/5d48bc06-26dd-4980-8e9b-08471d5c5c4a">
Easily monitor certificate expiration dates on multiple websites with the use of Zabbix agent 2 built-in functionality. The template is able to create items for each website listed in JSON using low level discovery. The first trigger is fired 7 days before a certificates expiration date. The second one is fired when a certificate is expired. 

This template is based on the official [Website certificate by Zabbix agent 2](https://git.zabbix.com/projects/ZBX/repos/zabbix/browse/templates/app/certificate_agent2?at=release/6.4).

Tested on Zabbix 6.4.4.
## Why two versions?
There are two versions of the template. The only difference between them is in the way they gather websites information. `Website_certificate_sender.yaml` is configured to recieve JSON via zabbix trapper. `website_certificate_macro.yaml` uses macro set in Zabbix web interface.
## How to use
- [How to use website_certificate_sender.yaml](https://github.com/dali-bor/Website-certificates-monitoring-template-for-Zabbix/blob/main/SENDER_SETUP.md)
- [How to use website_certificate_macro.yaml](https://github.com/dali-bor/Website-certificates-monitoring-template-for-Zabbix/blob/main/MACRO_SETUP.md)
