+++
author = "EnteleLAN"
title = "Home Lab Network Project - Milestone 1"
date = "2026-02-20"
description = "Home Lab Network Project - Milestone 1"
draft = "true"
+++

Building the Foundation&mdash;every stable network starts with discipline. Milestone 1 focuses on transforming an out-of-the-box default switch into a segmented and secure access layer. This may not be the flashy part of networking&mdash;but it is the part that determines whether everything built later is stable or fragile.

<br>

## Objective
Build the structural boundaries that all future services will depend on by establishing a segmented and secure Layer 2 access architecture.

This milestone focuses on:
* VLAN segmentation.
* Access port configuration.
* 802.1Q trunking.
* In-band management architecture.
* Baseline device hardening.
* Validation of segmentation boundaries.

The following are **not implemented** in this milestone:
* Inter-VLAN routing.
* WAN connectivity.
* DHCP services.
* Voice services.

Layer 3 will only be introduced after Layer 2 stability is proven.

<br>

## Hardware
* Cisco 2960 Catalyst switch.
* Cisco 2811 ISR (baseline configuration only; no routing enabled).

<br>

## VLAN Segmentation
The following VLANs are created:

| VLAN ID | Name | Purpose |
| :---: | :---: | :---: |
| 10 | DATA | End-user wired and wireless clients |
| 20 | VOICE | VoIP services |
| 88 | NATIVE | Native VLAN for 802.1Q trunks (no user traffic) |
| 99 | MGMT | In-band device management |
| 404 | INACTIVE | Unused switch ports (administratively shut down) |

### VLAN Design Notes
* VLAN 1 is **not used** for user traffic.
* Native VLAN changed from default VLAN 1 to VLAN 88.
* All access ports manually assigned&mdash;no dynamic negotiation.
* VLAN 404 used to administatively isolate unused ports.

This establishes clear traffic boundaries and eliminates ambiguity at Layer 2.

<br>

## 802.1Q Trunk Design
A single trunk link connects the 2960 access switch to the 2811 ISR.

### Trunk Characteristics:
* Encapsulation: 802.1Q.
* Native VLAN: 88.
* DTP disabled.
* Allowed VLAN list explicitly defined (10,20,99,88).

Explicit trunk configuration prevents unintended VLAN propagation, reduces VLAN hopping risk, and ensures deterministic behavior between devices.

<br>

## Access Port Configuration
### Data Ports
* Assigned to VLAN 10.
* Portfast enabled.
* BPDU Guard enabled.

### Voice Ports
* Access VLAN 10.
* Voice VLAN 20.
* Portfast enabled.
* BPDU Guard enabled.

### Unused Ports
* Assigned to VLAN 404.
* Administratively shut down.

No open ports; no default VLAN assignments; no dynamic behavior. This enforces containment at Layer 2.

<br>

## Management Architecture
This milestone formalizes in-band management.

### Management Characteristics
* Dedicated MGMT VLAN 99.
* SSH-only remote access.
* Telnet disabled.
* HTTP disabled.
* Console reserved for break-glass recovery only.
* Local user authentication with secret.
* Exec-timeout enforced.
* Management SVI configured in VLAN 99.

This ensures:
* Management traffic is logically separated from user traffic.
* Administrative access follows best practices.
* Remote access is encrypted and controlled.

Centralized AAA is intentionally deferred to a later milestone to maintain layered progression.

<br>

## Security Baseline
* `enable secret` configured.
* Local user authentication with secret.
* Domain name defined.
* RSA keys generated.
* VTY lines restricted to SSH.
* Exec-timeout configured.
* Unused services disabled.

## Router Baseline Configuration
The Cisco 2811 ISR remains functionally idle at Layer 3 during this milestone. This simplifies troubleshooting and preserves implementation layering.

The ISR is configured for:
* Hostname.
* Enable secret.
* SSH access.
* Basic interface descriptions.
* No sub-interfaces yet.
* No routing.
* No NAT.
* Baseline security.

Routing will be introduced only after the Layer 2 foundation is validated.

<br>

## Validation & Testing
Every configuration change was verified. Packet Tracer and the physical lab mirror one another as closely as possible.

### VLAN Validation
* `show vlan brief` to confirm segmentation.
  * Confirm ports are in correct VLANs.
  * Confirm VLAN 1 has no user-facing ports.

### Trunk Validation
* `show interfaces trunk`
  * Confirm 802.1Q encapsulation.
  * Confirm native VLAN is VLAN 88.
  * Confirm allowed VLAN list.
  * Confirm DTP is not negotiating.

### Management Validation
* SSH via VLAN 99.
* Confirm Telnet access fails.
* Confirm console remains accessible.
* Validate exec-timeout behavior.

### Security Validation
* Confirm unused ports are administratively shut down.
* Confirm BPDU Guard enabled on access ports.
* Confirm PortFast enabled.

<br>

## Failure Domain Acknowledgment
Redundancy is a future milestone&mdash;at this stage, the following are intentional single points of failure and are accepted constraints under Version 1 architecture:
* Single access switch = total LAN failure.
* Single trunk link = segementation failure if misconfigured.
* Single management path via VLAN 99.

## Acceptance
Milestone 1 is considered complete when:
* All VLANs are created and verified.
* Trunk behavior is deterministic and validated.
* Access ports behave as designed.
* Unused ports are secured.
* SSH-only management confirmed.
* Configuration saved and backed up.

<br>

## Lessons Learned
To be completed after full lab implementation.
<!--
This section will capture:
* Hardware vs. Packet Tracer behavior differences
* Native VLAN mismatch detection observations
* SSH configuration pitfalls
* Management VLAN reachability challenges
* Any unexpected trunk behavior
* VLAN propagation issues
-->

<br>

## Next Steps
* **Milestone 2**: Inter-VLAN Routing
  * Router-on-a-Stick implementation.
  * Default gateway configuration.
  * Initial Layer 3 traffic validation.
<!--
* **Milestone 3:** DHCP & Basic Services  
* **Milestone 4:** Internet Edge + NAT  
* **Milestone 5:** VoIP Integration
-->

<br>

## Commentary
Milestone 1 is about purpose, discipline, and restraint.

Without this foundation, inter-VLAN routing becomes messy, voice integration becomes unstable, security becomes reactive, WAN integration would be fragile, and troubleshooting becomes chaotic.

With this foundation traffic boundaries are clear, management is controlled, expansion is predictable, and every new service will be layered upon a stable foundation.

In network engineering, simplicity that is deliberate is more valuable than complexity that is impressive.

Milestone 1 is the beginning of building infrastructure with intention&mdash; not just connecting ports, but designing purpose.

<br>

<div class="commentbox"></div>

<script src="https://unpkg.com/commentbox.io/dist/commentBox.min.js"></script>
<script>
  commentBox('5668915749322752-proj', {
    backgroundColor: 'transparent',
    textColor: '#ffffff',
    subtextColor: '#ffffff',
    sortOrder: 'newest'
  });
</script>