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
-   [Control identity and access](ControlIdentiyAndAccess.md)
-   [Protect resources](ProtectResources.md)
-   [Detect & Respond - to threads](DetectAndRespond.md)
-   [Manage policies](ManagePolicies.md)

--- <!-- META -->
id: mra-cc-security
title: Security
sidebar_label: Security Overview
context: mra-cc
parent: mra-cc
child: mra-cc-security-control
prev:
next: mra-cc-interop
