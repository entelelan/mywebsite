+++
author = "EnteleLAN"
title = "Linux File System & Permissions"
date = "2025-09-12"
description = "linux file system & permissions"
tags = [
    "linux",
]
draft = "true"
+++

Howdy! Thanks for stopping by. I’m Moses and I’m a Network Engineer for an ISP.

## Linux File System

<table>
 <tr>
  <th>Location</th>
  <th>Description</th>
 </tr>
 <tr>
  <td>/</td>
  <td>Primary hierarchy and root directory of the entire file system.</td>
 </tr>
 <tr>
  <td>/bin</td>
  <td>System boot loader files.</td>
 </tr>
 <tr>
  <td>/boot</td>
  <td>System boot loader files.</td>
 </tr>
 <tr>
  <td>/dev</td>
  <td>Device files.</td>
 </tr>
 <tr>
  <td>/etc</td>
  <td>Host-specific configuration files.</td>
 </tr>
 <tr>
  <td>/home</td>
  <td>User home directory.</td>
 </tr>
 <tr>
  <td>/lib</td>
  <td>Shared library modules.</td>
 </tr>
 <tr>
  <td>/media</td>
  <td>Media files such as CD-ROM.</td>
 </tr>
 <tr>
  <td>/mnt</td>
  <td>Temporary mounted file systems.</td>
 </tr>
 <tr>
  <td>/opt</td>
  <td>Add-on application packages.</td>
 </tr>
 <tr>
  <td>/proc</td>
  <td>Automatically generated files</td>
 </tr>
 <tr>
  <td>/root</td>
  <td>Home directory for the root user.</td>
 </tr>
 <tr>
  <td>/run</td>
  <td>Run time program data.</td>
 </tr>
 <tr>
  <td>/sbin</td>
  <td>System binaries.</td>
 </tr>
 <tr>
  <td>/srv</td>
  <td>Site-specific data served on system.</td>
 </tr>
 <tr>
  <td>/sys</td>
  <td>Virtual directory info of system.</td>
 </tr>
 <tr>
  <td>/tmp</td>
  <td>Temporary files.</td>
 </tr>
 <tr>
  <td>/usr</td>
  <td>Ready-only user files.</td>
 </tr>
 <tr>
  <td>/var</td>
  <td>Temporary files.</td>
 </tr>
</table>

<br>
<br>

## Linux File Permissions
U = User  
G = Group  
W = World

r = Read  
w = Write  
x = Execute  
\- = No permissions

4 = read (r)  
2 = write (w)  
1 = execute (x)

The ***chmod*** command is used to modify file permissions.

