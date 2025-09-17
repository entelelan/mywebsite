+++
author = "EnteleLAN"
title = "Basic Cisco Switch Configuration"
date = "2025-09-12"
description = "Basic Cisco Switch Configuration"
tags = [
    "cisco",
]
draft = "true"
+++

### Basic Cisco Router Config
#### Device Configuration
<pre>
<code>enable
configure terminal
hostname hostname
enable secret password
no ip domain-lookup
line console 0
logging synchronous
exec-timeout timeout in minutes
end
clock set hh:mm:ss month day year</code>
</pre>

#### VLAN Configuration
<pre>
<code>configure terminal
vlan vlan_id
name native
vlan vlan_id
name mgmt
vlan vlan_id
name inactive_ports
exit
</code>
</pre>

#### Port Configuration
<pre>
<code>interface range interface range
shutdown
switchport mode access
switchport access vlan vlan_id
exit
</code>
</pre>

#### SSH Configuration
<pre>
<code>ip domain-name domain name
crypto key generate rsa
number of bits
ip ssh version ssh version
ip ssh time-out seconds
ip ssh authentication-retries number of retries
username username secret password
line vty 0 15
transport input ssh
transport output ssh
login local
logging synchronous
end
</code>
</pre>