+++
author = "EnteleLAN"
title = "Untitled"
date = "2025-09-12"
description = "Untitled"
tags = [
    "linux",
]
draft = "true"
+++

<!--
<h2>Google Router Configuration</h2>
<pre>
<code>configure terminal
hostname <font color=indianred><em><strong>hostname</strong></em></font>
interface <interface>
description <description>
ip address <ip address> <subnet mask>
no shutdown
interface <interface>
description <description>
ip address <ip address> <subnet mask>
no shutdown</code>
</pre>
-->

<!--
<h2>Google Switch Configuration</h2>
<pre>
<code>configure terminal
hostname <hostname>
interface vlan <vlan-id>
ip address <ip address> <subnet mask>
no shutdown
exit
ip default-gateway <ip address></code>
</pre>
-->

<!--
<h2>Google Server Configuration</h2>
<h3>IP Information</h3>
<li>IP Address: 8.8.8.8</li>
<li>Subnet Mask: 255.255.255.0</li>
<li>Default Gateway: 8.8.8.1</li>
<li>DNS Server: 8.8.8.8</li>

<h3>DNS Information</h3>
<li>Go to the Services tab</li>
<li>DNS: On</li>
<li>Name: www.test.com</li>
<li>IP Address: 8.8.8.8</li>
<li>Click Add</li>
<li>Highlight the entry</li>
<li>Click Save</li>
-->


[## IDF
\### Bay Face Layout / Rack Elevation
| Rack Unit # | Device Name | Device Type | Model | Serial # | MAC Address | Asset Tag # |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | 
| 1 | Empty | - | - | - | - | - | 
| 2 | Patch Panel | Copper Patch Panel | CPP98765432` | CPP987654321 | N/A | HLNAMTHQ-202511 |
| 3 | Empty | - | - | - | - | - | 
| 4 | HLNAMTHQ1AS | Layer 2 Switch | WS-C2960-24TT-L | FOC1010X104 | 00:01:63:20:9A:2A | HLNAMTHQ-202512 |
| 5 | Empty | - | - | - | - | - | 
| 6 | PDU | Power Distribution | AP8858NA4 | AP8858NA4 | N/A | HLNAMTHQ-202513 |
| 7 | Cable Tray | - | - | - | - | - |
| 8/39 | Empty | - | - | - | - | - | 
| 40/41 | UPSIDFR2 | UPS | SMTL750RM2UCUS | SMTL750RM2UCUS | N/A | HLNAMTHQ-202514 |
]: #

[### IDF Copper Patch Panel to Copper Wall Mounts
| Cable ID | Source Device | Source Port | Dest. Device | Dest. Port | Cable Type | Length | Color | Notes |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| CB-CPP2-PD3-CWMA-PD1 | Copper Patch Panel 2 | Punch Down 3 | Copper Wall Mount A | Punch Down 1 | Cat5e Strt | - | - | - |
| CB-CPP2-PD4-CWMA-PD2 | Copper Patch Panel 2 | Punch Down 4 | Copper Wall Mount A | Punch Down 2 | Cat5e Strt | - | - | - |
| CB-CPP2-PD5-CWMB-PD1 | Copper Patch Panel 2 | Punch Down 5 | Copper Wall Mount B | Punch Down 1 | Cat5e Strt | - | - | - |
| CB-CPP2-PD6-CWMB-PD2 | Copper Patch Panel 2 | Punch Down 6 | Copper Wall Mount B | Punch Down 2 | Cat5e Strt | - | - | - |
| CB-CPP2-PD7-CWMC-PD1 | Copper Patch Panel 2 | Punch Down 7 | Copper Wall Mount C | Punch Down 1 | Cat5e Strt | - | - | - |
| CB-CPP2-PD8-CWMC-PD2 | Copper Patch Panel 2 | Punch Down 8 | Copper Wall Mount C | Punch Down 2 | Cat5e Strt | - | - | - |
]: #

[### Copper Patch Panel to HLNAMTHQ1AS
| Cable ID | Source Device | Source Port | Dest. Device | Dest. Port | Cable Type | Length | Color | Notes |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| CB-CPP2-J1-HQ1AS-F0/1 | Copper Patch Panel | Jack 1 | HLNAMTGO1AS | F0/1 | Cat5e Crss | - | - | - |
| CB-CPP2-J2-GO1AS-F0/2 | Copper Patch Panel | Jack 2 | HLNAMTGO1AS | F0/2 | Cat5e Crss | - | - | - |
| CB-CPP2-J3-GO1AS-F0/3 | Copper Patch Panel | Jack 3 | HLNAMTGO1AS | F0/3 | Cat5e Strt | - | - | - |
| CB-CPP2-J4-GO1AS-F0/4 | Copper Patch Panel | Jack 4 | HLNAMTGO1AS | F0/4 | Cat5e Strt | - | - | - |
| CB-CPP2-J5-GO1AS-F0/5 | Copper Patch Panel | Jack 5 | HLNAMTGO1AS | F0/5 | Cat5e Strt | - | - | - |
| CB-CPP2-J6-GO1AS-F0/6 | Copper Patch Panel | Jack 6 | HLNAMTGO1AS | F0/6 | Cat5e Strt | - | - | - |
| CB-CPP2-J7-GO1AS-F0/7 | Copper Patch Panel | Jack 7 | HLNAMTGO1AS | F0/7 | Cat5e Strt | - | - | - |
| CB-CPP2-J8-GO1AS-F0/8 | Copper Patch Panel | Jack 8 | HLNAMTGO1AS | F0/8 | Cat5e Strt | - | - | - |
]: #

[### Copper Wall Mounts to Endpoints
| Source Device | Dest. Device | MAC Address |
| :---: | :---: | :---: |
| CWMA-J1 | IP Phone | 0060.70AE.5D5A |
| CWMA-J2 | IP Phone | 000A.415B.83C4 |
| CWMB-J1 | IP Phone | 0060.7080.9EE4 |
| CWMB-J2 | IP Phone | 000B.BEAD.8CBE |
| CWMC-J1 | IP Phone | 000A.F3E2.5D66 |
| CWMC-J2 | IP Phone | 00E0.F73B.C366 |
]: #

End-Devices
| Device Name | OS | Services | MAC Address | IP Address | Default Gateway | DNS | VLAN |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |

Device Layout
## HLNAMTHQ1CR
| Device Name | Model | Device Type | Location | IOS | Flash | License | Serial Number |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| YESTMTDR1CR | ISR 2911 | Internet Router | MDF Bldg. A Main Floor Rm. 100 | Cisco IOS Software, Version 15.1(4)M4 | flash0:c2900-universalk9-mz.SPA.151-1.M4.bin | ipbasek9 uck9 | FTX1524X00B- |

| Interface | Description | IPv4 Address | Default Gateway | IPv6 Address | Default Gateway | MAC Address | Routing |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| G0/0 | - | - | - | - | - | - | - |
| G0/1 | Router-on-a-stick to YESTMTDR1AS interface G0/1 | -  | - | - | - | - | - |
| G0/1.10 | Sub-Interface for Data VLAN 10 | 10.10.10.0/24 | 10.10.10.1 | - | - | - | - |
| G0/1.20 | Sub-Interface for Voice VLAN 20 | 10.10.20.0/24 | 10.10.20.1 | - | - | - | - |
| G0/1.88 | Sub-Interface for Native VLAN 88 | - | - | - | - | - | - |
| G0/2 | - | - | - | - | - | - | - |
| G0/0/0 | Link to ISP | 200.100.10.1/30 | - | - | - | - | - |

## HLNAMTHQ1VR
| Device Name | Model | Device Type | Location | IOS | Flash | License | Serial Number |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| YESTMTDR1CR | ISR 2911 | Internet Router | MDF Bldg. A Main Floor Rm. 100 | Cisco IOS Software, Version 15.1(4)M4 | flash0:c2900-universalk9-mz.SPA.151-1.M4.bin | ipbasek9 uck9 | FTX1524X00B- |

| Interface | Description | IPv4 Address | Default Gateway | IPv6 Address | Default Gateway | MAC Address | Routing |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| G0/0 | - | - | - | - | - | - | - |
| G0/1 | Router-on-a-stick to YESTMTDR1AS interface G0/1 | -  | - | - | - | - | - |
| G0/1.10 | Sub-Interface for Data VLAN 10 | 10.10.10.0/24 | 10.10.10.1 | - | - | - | - |
| G0/1.20 | Sub-Interface for Voice VLAN 20 | 10.10.20.0/24 | 10.10.20.1 | - | - | - | - |
| G0/1.88 | Sub-Interface for Native VLAN 88 | - | - | - | - | - | - |
| G0/2 | - | - | - | - | - | - | - |
| G0/0/0 | Link to ISP | 200.100.10.1/30 | - | - | - | - | - |

## HLNAMTHQ1CS
| Device Name | Model | Device Type | Location | IOS | Flash | License | Serial Number |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | --- |
| YESTMTDR1AS | Catalyst 2960 | LAN Access Switch | IDF Bldg. A Floor 2 Rm. 200

| VLAN Number | VLAN Name | Description |
| ---- | --- | --- |
| 10 | Data | User data traffic |
| 20 | Voice | User voice traffic |
| 88 | Native | Untagged traffic |
| 99 | Management | Management traffic |
| 404 | Inactive | Port(s) not in use |

| Interface | Description | Switchport Type | VLAN |
| ---- | ---- | ---- | ---- |
| F0/1 | | Access | 10 & 20 |
| F0/2 | | Access | 10 & 20 |
| F0/3 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/4 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/5 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/6 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/7 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/8 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/9 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/10 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/11 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/12 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/13 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/14 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/15 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/16 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/17 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/18 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/19 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/20 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/21 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/22 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/23 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/24 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| G0/1 | Trunk to YESTMTDR1CR G0/1 | Trunk | 88 |
| G0/2 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| SVI 99 | Remote management | - | - |

## HLNAMTHQ2CS
| Device Name | Model | Device Type | Location | IOS | Flash | License | Serial Number |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | --- |
| YESTMTDR1AS | Catalyst 2960 | LAN Access Switch | IDF Bldg. A Floor 2 Rm. 200 |

<br>

| VLAN Number | VLAN Name | Description |
| ---- | --- | --- |
| 10 | Data | User data traffic |
| 20 | Voice | User voice traffic |
| 88 | Native | Untagged traffic |
| 99 | Management | Management traffic |
| 404 | Inactive | Port(s) not in use |

<br>

| Interface | Description | Switchport Type | VLAN |
| ---- | ---- | ---- | ---- |
| F0/1 | | Access | 10 & 20 |
| F0/2 | | Access | 10 & 20 |
| F0/3 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/4 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/5 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/6 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/7 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/8 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/9 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/10 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/11 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/12 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/13 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/14 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/15 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/16 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/17 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/18 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/19 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/20 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/21 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/22 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/23 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| F0/24 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| G0/1 | Trunk to YESTMTDR1CR G0/1 | Trunk | 88 |
| G0/2 | \*\*\*NOT IN USE\*\*\* | Access | 404 |
| SVI 99 | Remote management | - | - | 

## Router Configuration
### Basic Device Configuration
enable
configure terminal
hostname <hostname>
enable secret <password>
no ip domain-lookup
line console 0
logging synchronous
exec-timeout <minutes>
end
clock set <hh:mm:ss Mmm DD YYYY>

### SSH Configuration
configure terminal
ip domain-name <domain name>
crypto key generate rsa

ip ssh version 2
ip ssh time-out <seconds>
ip ssh authentication-retries <number of retries>
username <username> secret <password>
line vty 0 15
logging synchronous
login local
transport input ssh
transport output ssh
exit

### DHCP Configuration
ip dhcp excluded-address <starting_ip ending_ip>
ip dhcp excluded-address <starting_ip ending_ip>
ip dhcp pool <dhcp_pool_name>
network <network_ip_address> <subnet mask>
default-router <gateway_ip>
dns-server <dns_server_ip>
ip dhcp pool <dhcp_pool_name>
network <network_ip_address> <subnet mask>
default-router <gateway_ip>
option 150 ip <voice_gateway_ip>
exit

### Router-on-a-Stick Configuration
interface <sub-interface>
description <description>
encapsulation dot1q <vlan-id>
ip address <gateway_ip> <subnet mask>
interface <sub-interface>
description <description>
encapsulation dot1q <vlan-id>
ip address <gateway_ip> <subnet mask>
interface <sub-interface>
description <description>
encapsulation dot1q <vlan-id> native
interface <interface>
no shutdown
exit

### Telephony Configuration
license boot module c2900 technology-package uck9

end
copy running-config startup-config
reload

enable

configure terminal
telephony-service 
max-ephones <number of phones>
max-dn <number of phones>
ip source-address <voice_gateway_ip> port 2000
exit
ephone-dn 1
number 1001
ephone-dn 2
number 1002
exit
ephone 1
type 7960
mac-address <phone mac address>
button 1:1
ephone 2
type 7960
mac-address <phone mac address>
button 1:2
exit

### NAT/PAT Configuration
configure terminal
interface <interface>
ip address <ip address> <subnet mask>
no shutdown
exit
ip route 0.0.0.0 0.0.0.0 <next-hop ip>
access-list 1 permit <network ip> <wildcard mask>
access-list 1 permit <network ip> <wildcard mask>
ip nat inside source list 1 interface <interface> overload
interface <sub-interface>
ip nat inside
interface <sub-interface>
ip nat inside
interface <interface>
ip nat outside
end

copy running-config startup-config

## Switch Configuration
### Basic Device Configuration
enable
configure terminal
hostname <hostname>
enable secret <password>
no ip domain-lookup
line console 0
logging synchronous
exec-timeout <minutes>
end
clock set <hh:mm:ss Mmm DD YYYY>

### VLAN Configuration
configure terminal
vlan <vlan-id>
name <vlan name>
vlan <vlan-id>
name <vlan name>
vlan <vlan-id>
name <vlan name>
vlan <vlan-id>
name <vlan name>
vlan <vlan-id>
name <vlan name>
exit

### Port Configuration
interface range <interface range>
shutdown
switchport mode access
switchport access vlan <vlan-id>
interface <interface>
shutdown
switchport mode access
switchport access vlan <vlan-id>
interface range <interface range>
switchport mode access
switchport access vlan <vlan-id>
switchport voice vlan <vlan-id>
interface <interface>
description <description>
switchport mode trunk
switchport trunk native vlan <vlan-id>
switchport trunk allowed vlan <vlan-ids>
exit

### SSH Configuration
ip domain-name <domain name>
crypto key generate rsa 

ip ssh version 2
ip ssh time-out <seconds>
ip ssh authentication-retries <number of retries>
username <username> secret <password>
line vty 0 15
logging synchronous
login local
transport input ssh
transport output ssh
end
copy running-config startup-config
