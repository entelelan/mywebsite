+++
author = "EnteleLAN"
title = "Junos Device Config"
date = "2025-09-12"
description = "junos device config"
tags = [
    "linux",
]
draft = "true"
+++

cli  
configure  
set system host-name <device_name>  
set system domain-name <domain_name.com>  
set interfaces fxp0 unit 0 family inet address <ip-address/cidr>  
set system name-server <ip_address>  
set system root-authentication plain-text-password  
set system login message "----------------------------------------\nWARNING: Unauthorized access prohibited.\n----------------------------------------"  
set system login user <username> class <privilege_class>  
set system login user <username> full-name <"full_name">  
set system login user <username> uid <uid>  
set system login user <username> authentication plain-text-password  
\> set date YYYYMMDDHHMM  
\# set time-zone <GMT-5>  
set interfaces <interface> unit <unit> family inet address <ip_address/cidr>  
set lo0 unit <unit> family inet address <ip_address/32>  

help topic system domain-name  
help reference system domain-name  

show version  
show version detail  
show chassis hardware  
show chassis hardware detail  
show interfaces terse  
show vlans  
show log messages  
show system uptime  
show system commit  
show cli authorization  