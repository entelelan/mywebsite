+++
author = "EnteleLAN"
title = "Configuring an IP Address in Linux"
date = "2025-09-12"
description = "linux ip config"
tags = [
    "linux",
]
draft = "true"
+++

STATIC  
network:  
  version: 2  
  ethernets:  
    enx0051b578211:  
      dhcp4: false  
      addresses:  
        - 192.168.1.100/24  
      gateway4: 192.168.1.1  
      nameservers:  
        addresses:  
          - 8.8.8.8  
          - 1.1.1.1  
 
DHCP  
network:  
  version: 2  
  ethernets:  
    enx0051b578211:  
      dhcp4: true  
      optional: true  