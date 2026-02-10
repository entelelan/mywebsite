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