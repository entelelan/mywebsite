+++
author = "EnteleLAN"
title = "Configuring a DHCP Server"
date = "2025-09-12"
description = "Ubuntu DHCP Server"
tags = [
    "linux",
]
draft = "true"
+++

look for your ethernet int - mine is enp3s0 using ip a <enter>
- sudo apt install isc-dhcp-server
- sudo nano /etc/default/isc-dhcp-server
- sudo nano /etc/dhcp/dhcpd.conf
- sudo systemctl restart isc-dhcp-server.service
- sudo systemctl status isc-dhcp-server.service
- sudo su
- systemctl restart isc-dhcp-server.service
- systemctl status isc-dhcp-server.service
- sudo netstat -anp | grep dhcp
- sudo ufw allow <port/protocol>
- sudo ufw status

network:
  version: 2
  renderer: networkd
  ethernets:
    enp3s0:
      addresses:
        - 192.168.1.2/24
      gateway4: 192.168.1.1
      nameservers:
          addresses: [1.1.1.1, 1.0.0.1]

systemctl status tftpd-hpa
systemctl status rsyslog
systemctl status isc-dhcp-server.service
tail -f /var/log/syslog