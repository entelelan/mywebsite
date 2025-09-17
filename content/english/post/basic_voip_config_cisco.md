+++
author = "EnteleLAN"
title = "Basic Cisco VoIP Configuration"
date = "2025-09-12"
description = "Basic Cisco VoIP Configuration"
tags = [
    "cisco",
]
draft = "true"
+++

### Router Configuration
#### VLAN 10
<pre>
<code>Router(config)# interface f0/0
Router(config-if)# no shutdown
Router(config)# interface f0/0.10
Router(config-subif)# encapsulation dot1q 10
Router(config-subif)# ip address 192.168.10.1 255.255.255.0</code>
</pre>

#### VLAN 20
<pre>
<code>Router(config)# interface f0/0.20
Router(config-subif)# encapsulation dot1q 20
Router(config-subif)# ip address 192.168.20.1 255.255.255.0</code>
</pre>

#### Voice DHCP Pool
<pre>
<code>Router(config)# ip dhcp excluded-address 192.168.10.1
Router(config)# ip dhcp excluded-address 192.168.20.1
Router(config)# ip dhcp pool voice
Router(dhcp-config)# network 192.168.10.0 255.255.255.0
Router(dhcp-config)# default-router 192.168.10.1
Router(dhcp-config)# option 150 ip 192.168.10.1</code>
</pre>

#### Data DHCP Pool
<pre>
<code>Router(config)# ip dhcp pool data
Router(dhcp-config)# network 192.168.20.0 255.255.255.0
Router(dhcp-config)# default-router 192.168.20.1</code>
</pre>

#### Telephony Service
<pre>
<code>Router(config)# telephony-service
Router(config-telephony)# max-ephones 2
Router(config-telephony)# max-dn 2
Router(config-telephony)# auto assign 1 to 5
Router(config-telephony)# ip source-address 192.18.10.1 port 2000</code>
</pre>

#### ephone
<pre>
<code>Router(config)# ephone 1
Router(config-ephone)# type 7960
Router(config-ephone)# ex
Router(config)# ephone 2
Router(config-ephone)# type 7960
Router(config)# ephone-dn 1
Router(config-ephone-dn)# number 1001
Router(config)# ephone-dn 2
Router(config-ephone-dn)# number 1002</code>
</pre>

### Switch Configuration
<pre>
<code>Switch> enable
Switch# configure terminal
Switch(config)# interface range f0/2-3
Switch(config-if-range)# switchport mode access
Switch(config-if-range)# switchport access vlan 20
Switch(config-if-range)# switchport voice vlan 10
Switch(config)# interface f0/1
Switch(config-if)# switchport mode trunk</code>
</pre>