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

banner motd\
\#\
\---------------------------------------------------------------------------------------\
This network device is private property of my home lab.
WARNING: Unauthorized access is strictly prohibited.
If you are not authorized to access this device, disconnect now!
Unauthorized use is subject to civil or criminal prosecution under applicable law.\
\---------------------------------------------------------------------------------------\
\#

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

ip ssh version <ssh version>
ip ssh time-out <seconds>
ip ssh authentication-retries <number of retries>
username <username> secret <password>
line vty 0 15
transport input ssh
transport output ssh
login local
logging synchronous
end

copy running-config startup-config