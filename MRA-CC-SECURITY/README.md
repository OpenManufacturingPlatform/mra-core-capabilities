# Security

IT and OT integration brings its own set of security challenges in the
Industrial context as these were earlier considered to be separate and
isolated networks. The Security capability ensures that complete
connected system is secured end to end.

To enable a robust security mechanism, it is advisable to also take best
practices suggested by international standard agencies (ISO 27001, ISO
27002, ISO 27017, IEC 62443) and then apply additional measures and
approaches on top of it to align it to industrial context. It might also
be necessary to deviate from standards, e.g. the strict communication
hierarchy defined by IEC62433 is diluted by Industrial IoT solutions.
Modern concepts like Zero Trust Networks will become more and more
important.

An Open Manufacturing Platform needs Security Controls that:
-   Are Form factor independent
-   Offer End to End Visibility (Edge \<-\> DC \<-\> Cloud)
-   Are Programmable, Intent driven
-   Are good to handle, Reduce the complexity
-   Offer atomic visibility to Reduce the attack surface in the endpoint
-   Decoupling Security Policy from cabling (Control/data Plane)
-   Use industry standard protocols

As we are getting new form factors like containers and VMs steering the
shop floor, running on Container Hosts and Hypervisors, and securing
these in an omniscient and efficient way. Security controls need to move
closer to the workloads to the edge, and ideally must be moved into the
platform and offer the possibility to be interconnected and automated
via API.

Security is a vast and critical topic. We grouped the capabilities into
the main sections:
-   Control identity and access
-   Protect resources
-   Detect & Respond - to threads
-   Manage policies


## Protect resources \[Bernd/Alexandra/Ashish\]

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

## Detect & Respond to Threads

### Intrusion Detection

This capability helps in detecting proactively the vulnerability
caused by looking at the network traffic. This acts as a line of
defense to identify early signs of malicious activities and gives
ability to effectively report and respond. Usually, the threats are
identified by a standard signature-based mechanism. In this the
traffic patterns are analyzed based on already known specific
patterns. However, this approach has a limitation of missing new
attacks for which no signature exists. Looking at today's threat
landscape it is better to also look at capabilities which enable an AI
based approach which uses machine learning to create a model which
helps to identify still unknown attacks.

### Vulnerability Scanning

Ability to identify vulnerabilities within the network is a critical
line of defense to proactively identify scenarios of security weakness
which can lead to threats. This is enabled by some of the tools which
help in scanning and identifying threats. Usually, it does it by
scanning the whole network to create an inventory of the systems which
are connected and then builds up a knowledge base, e.g., operating
system, software running on each node, open ports, accounts etc. It is
also important to have a constantly enriched knowledge base against
which this inventory and its data needs to be compared to identify
vulnerabilities. This becomes much more critical in industrial setup,
as in majority of the scenarios unlike the IT ecosystem, the inventory
of assets is either not created or is not updated due to lack of
focused solutions for this area. This could mean like for example a
PLC may be running a very outdated and unpatched OS, some of the ports
on a PLC may be open although not required, a laptop may be connected
on the same network as manufacturing line with higher user privileges,
a new program may be loaded to a PLC. All these scenarios open up a
huge attack vector. While such a capability is a standard in IT
networks, but manufacturers should look into enabling this capability
in OT network as well. For this to work this capability should be
capable of understand the OT system and network, its specific
protocols, its processes, and capabilities of various automation OEM
systems.

### Threat Intelligence & Monitoring

Threat Intelligence & Monitoring is a capability which draws its
features from multiple other security capabilities like logging,
monitoring, vulnerability scanning, IDS, IPS etc. This is focused on
collecting and analyzing information about the current and potential
attack vectors and is helpful towards improving the security posture.
It helps to play a major role in helping detect a potential attack
early enough to either prevent or limit its impact. It is important
that this capability is able to collect and process data from multiple
existing sources and solutions, is able to process data in multiple
formats, is able to add context between the data, and is able to
identify thread indicators. It is important for the organization to
have capability to constantly research new threats emerging outside
and augment this information. In case organization lacks this in house
skills of research and analysis, it can also tap into solution vendors
specializing in this area.

### Risk & Vulnerability Management

In this context where the networks handling IT and OT assets have
started to connect, it is important to have the capability to look at
the entire attach surface. In an approach of looking at only
vulnerabilities in isolation may have an impact of missing out the
vulnerabilities which pose more risk or threat and which needs to be
prioritized. Hence looking at vulnerabilities with the Lense of the
risk helps to put a context and helps to prioritize and group them
into areas of focus. Also, this process needs to be automatic and
dynamic so that it can change the risk score based on the shifting
threat landscape. Overall, this capability encompasses other aspects
to enable the complete cycle of Discovering, Classification,
Prioritization, and Remediation.

### Monitoring

Monitoring is a foundational capability which helps analyze and
process billions of events and alerts being generated by various
systems which can be running in the centralized/cloud system, or in
the plant eco system (including production support systems, equipment,
devices, gateways etc.). This allows to analyze this diverse set of
data to optimize performance, remediate problems, and also to monitor
for security incidents and events. Monitoring can go from simple
reporting, to a complex one which also includes aspects of machine
learning to filter out noise from information.

### Logging

Logging is one of the most fundamental capabilities which essentially
drives a lot of upper-level security capabilities. As most of the
capabilities would depend on the underlying systems to provide it with
enough data to identify patters. For example, event logs can be used
for forensic works to look at audit trails when doing the root cause
analysis. Hence it is important that all systems provide a consistent
and controllable access to logs. Also, a centralized logging framework
helps to connect various systems and identify patterns and
correlations helping in proactively identifying threats

## Manage Policies

Security policy are set of rules that define the security objectives in
terms of what should be protected from whom under which the conditions.
A platform must provide effective monitoring of these policies and sure
their enforcement. Security policies inherently help to standardize
their enforcements across organization in a consistent way. Industry
specific governmental and regulatory requirements (e.g., NIST, HIPPA)
might apply additionally. Security policy have broad impact on elements
like system resources, authentication & authorization, system Integrity
and many others.

Regular and sometimes continuous auditing is needed to ensure compliance
with security policies, to avoid security posture degrade over time.

### Security Policies

Security policy are set of rules that define the security objectives
in terms of what do we want to protect, from whom, and the conditions.
Effective monitoring of policies in terms of effectiveness and
enforcement is important. Security policies help standardize the
enforcements across organization in a consistent way. Depending upon
industries, there may be a need to align the policies with
governmental and regulatory requirements (e.g. NIST, HIPPA). Security
policy would broadly control: System resources, Authentication,
Authorization, Data Integrity, System Integrity, Auditing,
Confidentiality.

### Network Policies

Network policy is a specific kind of Security Policy, which define the
rules that govern the behaviors of network and connected devices.
Having the ability to define policy for network also helps to automate
and respond more quickly at the network level on the changing security
requirement and posture. Broadly various policies under this cover:
Access to network, resources access, allowed applications, define and
allocate Quality of Service, traffic routing and control

### Auditing

Auditing is needed to make sure that the security posture doesn't
degrade over time. Ideally auditing needs to be aligned to some of the
industry standard benchmarks (e.g., Center for Internet Security
(CIS), OWASP, ISA/IEC 62443 etc.). This industry alignment helps to
improve the security program as it allows the learnings across the
wider industry space and also helps compare the security state with
other peers. So even if the current security program is not tied to
any of these standard benchmarks, it still will give a good guidance
to define own program and compare with what others are doing. However,
another aspect which is also important is that after the definition of
these, there has to be a capability available to continuously assess,
review, and monitor the compliance status across the space under
scope.

### Secure the Software Supply Chain

Secure Software Supply Chain is in theory good imperative policy
target, but reality shows it is often not doable or an illusion. There
may be contractual and due diligence things that can be done in the
supply chain, but reality shows that you cannot trust software that
you bought, that your 3rd party ISV is always guaranteed error free.
Also an in-house development team is vulnerable to Typosquatting type
of attacks and can introduce inadvertently malicious code.

A secure software supply chain (SSSC) defines and enforces standards
for the whole chain – from sourcing of base images, libraries,
frameworks, 3d party software via static code analysis and security
scanning to deployment and operations. As new vulnerability are
identified after deployment, continuous scanning is required to be
alerted and necessary controls can be activated.


--- META
id: mra-cc-security
title: Security
sidebar_label: Security Overview
context: mra-cc
parent: mra-cc
child: mra-cc-security-control
prev:
next: mra-cc-interop
---
