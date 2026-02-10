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

banner motd\
\#\
\---------------------------------------------------------------------------------------\
This network device is private property of my home lab.
WARNING: Unauthorized access is strictly prohibited.
If you are not authorized to access this device, disconnect now!
Unauthorized use is subject to civil or criminal prosecution under applicable law.\
\---------------------------------------------------------------------------------------\
\#

### SSH Configuration
configure terminal
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
<!--- auto assign <number to number> optional for auto assignment --->
ip source-address <voice_gateway_ip> port 2000
exit
<!--- ephone <number> 
type <IP phone model>
number <extension> 
add this portion if using auto assignment --->
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