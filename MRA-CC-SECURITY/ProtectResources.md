## Protect resources 

In spite of various security control measures, we still seen
industrial environments being subjected to sophisticated
cyber-attacks. Active protection is required to mitigate the risks.
Network segmentation becomes important as a countermeasure to control
the blast radius and containing it from spreading to larger network.
This segmentation covers separating out the layers in Purdue model,
and also within the layers as well creating smaller segments.

### Protect Networks

Segmented network zones are key to control blast radius. Transition
points between networks with firefalls provide control authority and
enable detection of malicious activities using anomaly patterns. It is
important to ensure that specialized firewalls are enabled for the
industrial scenarios. These firewalls should also understand OT
protocols like DNP, CIP, Modbus etc. which are being used by
automation vendors. This is important to enable the firewall to secure
the OT environment. Esp. Shop floor networks are frequently “secure by
definition”. In a highly access controlled manufacturing site this
“the network is secure” approach is comprehensible. However, it should
be avoided and translated into a “zero trust, always verify” approach.

### Protect Data

Data Confidentiality capability ensures that through various controls
placed, the access to data is controlled to only those which are
specifically authorized for that. In order to protect critical data,
manufacturers should ensure that end-to-end encryption with strong
encryption keys is implemented along the entire value chain spanning
from the edge to cloud. This holds true for data at rest and data in
motion. Above mentioned PKI capabilities are helpful for key
management.

### Protect Endpoints

All endpoints need protection and management. Mobile Devices,
Industrial PCs, HMI systems. All are vulnerable to attacks, thus all
need protection. Imagine the HMI system of a critical machine being
hijacked by a ransomware attack.

### Protect the Operating System (OS)

No good security concept can leave out security countermeasures in or
around the OS System. The role of the classical guest operating system
is changing since two decades massively. A classical OS is something
like Linux or Windows or Macintosh. But the verge of Virtualization
and Containerization, that serve as the orchestration, abstraction and
platform layer for other classical OSes and their Applications
(Hypervisor & Central Management / Container Hosts & Caas) degraded
these classical OSes as VMs guests. If you carve out even more
binaries of a classical OS, to a minimal viable OS (Container Host) to
launch tailored massively distributed applications (containers), also
these need special security considerations. In contrast to VMs on a
hypervisor (x86 guest OS virtualization), containers are a form of
kernel level virtualization and provide less isolation guarantees on
the same container host.

No matter whether it is a hypervisor or a container steering a machine
on the shopfloor, they are additional layers, which are a high value
attack target and therefore need to be hardened and operated with
care. They are so to say the privileged OS for others OS form factors
(VM/Container). So it is imperative to develop good operating and
hardening strategies with special due diligence at this layer.

Is even more important than on Guests. Still nowadays you often find
in the shopfloors very outdated Operating Systems that are not
maintained be the software supplier, and no new patches are developed
to patch vulnerabilities leaving them vulnerable. Behavioral
Whitelisting Solutions are a good technology area to ensure that only
intended and known good software is used in the correct manner inside
the outdated OS. They allow to run what is good and everything else is
being execution blocked per default. Device control is also mandatory
at operator machines on the shop floor.

--- <!-- META -->
id: mra-cc-security-protect
title: Protect Resources
sidebar_label: Protect Resources
context: mra-cc > mra-cc-security
parent: mra-cc-security
child:
prev: mra-cc-security-control 
next: mra-cc-security-detect
