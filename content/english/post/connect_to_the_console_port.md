+++
author = "EnteleLAN"
title = "Connect to the Console Port"
date = "2025-09-12"
description = "Connect to the Console Port"
tags = [
    "cisco",
]
draft = "true"
+++

### Connect to the Console Port with macOS

---

**Step 1** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Launch the **Terminal** application.  
**Step 2** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Connect the console cable from your macOS device to the console port on the chassis.  
**Step 3** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Enter the following commands to find the USB connection:
<pre>
<code>% cd /dev
% ls -ltr /dev/*usb*</code>
</pre>
**Step 4** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Connect to the USB port with the following command followed by the chassis USB port speed:
<pre>
<code>% screen /dev/tty.insert_usb_port_name_here 9600</code>
</pre>
**Step 5** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;To disconnect press ***CTRL+a*** followed by ***d*** or ***CTRL+\***.

<br>

### Connect to the Console Port with Linux

---

**Step 1** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Launch the **Terminal** application.  
**Step 2** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Connect the console cable from your Linux device to the console port on the chassis.  
**Step 3** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Enter the following commands to find the USB connection:
<pre>
<code># cd /dev
% ls -ltr *ttyUSB*</code>
</pre>
**Step 4** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Connect to the USB port with the following command followed by the chassis USB port speed:
<pre>
<code>% screen /dev/tty<em>insert_usb_port_name_here</em> 9600</code>
</pre>
**Step 5** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;To disconnect press ***CTRL+a*** followed by ***:quit***.

<br>

### Connect to the Console Port with WSL

---

**Step 1** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Launch the **Terminal** application.  
**Step 2** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Connect the console cable from your Linux device to the console port on the chassis.  
**Step 3** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Enter the following commands to find the USB connection:
<pre>
<code># cd /dev
% ls -ltr *ttyUSB*</code>
</pre>
**Step 4** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Connect to the USB port with the following command followed by the chassis USB port speed:
<pre>
<code>% screen /dev/tty<em>insert_usb_port_name_here</em> 9600</code>
</pre>
**Step 5** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;To disconnect press ***CTRL+a*** followed by ***:quit***.