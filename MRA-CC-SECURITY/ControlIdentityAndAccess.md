
## Control Identify and Access
Identity and access need to be controlled for user, system, machine,
devices etc. User Federation and Identity Brokering are needed to
integrate existing repositories. Modern authentication mechanisms like
Multi Factor Authentication, Step-Up-Authentication, FIDO2 security keys
can help to resolve conflicts with operational needs of fast and easy
access.

Certificates are used to establish trust, to identify users and devices
(in general: end point). They are part of a Public Private Key
Infrastructure – PKI) and the Certificate Authority. They take care of
provisioning, inventory management, monitoring, renewal, and revocation
of certificates.

Once identity is verified, access and privileges to the resources is
granted and enforced. Least privilege access principles should be
followed. Access control governs all the available resources and
workloads, and can be either pure policy based, or time bound, or based
on certain conditions (e.g., role based, source location, time of day
etc.), or a combination of them.

### Manage Identity

This capability assists in associating a user, system, machine, or
process with a unique identity which is global to the whole system.
This enables the system to know with whom it is interacting so that
necessary access can be provided. Identities should be maintained in a
secured system (e.g., Active Directory for user identities).
Additionally, in IoT context, each physical device needs to have a
specific identity assigned to it, if it has to connect and interact
with the system. Along with this, it is advisable to enable a
“hardware root of trust” for physical devices to secure this identify
at source.

Non-Personalized Identities (“User: NightShift”) or no identities at
all should be avoided to allow for zero trust concepts. This often
conflicts with operational needs of fast and easy access, e.g. to an
HMI interface of a machine.

### Authenticate Identities

This helps in “proving” that the identity is valid. This is where the
system starts to trust the end point. For example, this could be via
password comparison between what is provided versus what is available
in the system. Depending upon the context, authentication can cover
various mechanisms like Password based or Multi Factor Authentication
(MFA) based. In today’s security posture, it is advisable to have MFA
for added security which brings an additional second layer. This
second layer can be enabled via an authenticator App, SMS, Voice,
OAUTH software, hardware tokens, and FIDO2 security keys etc. The
authentication does not stop at user level but covers all entities
which need to connect. For devices it is advisable to have a password
less authentication mechanisms, enabled by certificates (e.g., X.509)
which are secured by a TPM module. It is also important for the system
to have capability to enable renewal of credentials. Similarly, for
the external systems who need to interact (system to system
interaction) can utilize token-based authentication (e.g., OAUTH, SAML
etc.)

### Control Access & Authorization

This enables the access rights and privileges to the resources once
its identity has been verified. This capability enables mechanism for
a “Least privilege access”. The access control governs all the
available resources and workloads, and can be either pure policy
based, or time bound, or based on certain conditions (e.g., role
based, source location, time of day etc.), or a combination of them.

### Manage Certificates

Certificates are used to establish trust, to identify users and
devices (in general: end point). They are part of a Public Private Key
Infrastructure – PKI) and the Certificate Authority. They take care of
Provisioning, Inventory Management, Monitoring, Renewal, and
Revocation of certificates.

--- <!-- META -->
id: mra-cc-security-control
title: Control Identity and Access
sidebar_label: Control Identity and Access
context: mra-cc > mra-cc-security
parent: mra-cc-security
child:
prev:  
next: mra-cc-security-protect
