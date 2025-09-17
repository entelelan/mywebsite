+++
author = "EnteleLAN"
title = "Routing vs. Routed Protocols"
date = "2025-09-12"
description = "Routing vs. Routed Protocols"
tags = [
    "linux",
]
draft = "true"
+++

Routing protocols and routed protocols are two types of protocols that are used in computer networks. A protocol is a set of rules and standards that define how devices communicate with each other.

A "routing protocol" is a protocol that helps routers exchange information about the topology reachability of the network. Routing protocols enable routers to learn about the best paths to forward packets to their destinations. Routing protocols also update routers when there are changes in the network, such as link failures or new connections. Examples of routing protocols are RIP, OSPF, EIGRP, BGP, etc.

A "routed protocol" is a protocol that carries user data between end devices, such as computers, servers, printers, etc. Routed protocols provide logical addressing to end devices, which routers use to forward packets based on their destination addresses. Routed protocols also encapsulate and de-encapsulate data packets with headers and trailers that contain information such as source and destination addresses, checksums, etc. Examples of routed protocols are IP (both IPv4 and IPv6), IPX AppleTalk, etc.

The main difference between routing protocols and routed protocols are:
- Routing protocols are used by routers to exchange routing information, while routed protocols are used by end devices to send and receive data packets.
- Routing protocols operate at the network layer (Layer 3) of the OSI model, while routed protocols can operate at different layers depending on their functions.
- Routing protocols do not carry user data, while routed protocols do.
- Routing protocols are not assigned to interfaces, while routed protocols are.