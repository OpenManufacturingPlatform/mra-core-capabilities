## Manage Device Lifecycle

\[OMP IOTCON-02 2021\] defines device lifecycle phases and management
capabilities:

<img src="/assets/images/DEVICEMMGT_Phases.png" width="50%" />

### Provision devices

For most companies the differences between the use case to be supported
will lead to a selection of different device types rather than a single
device. The challenge is to balance a cost-efficient solution with a
hardware standardization approach. As selected use cases will be
executed on the same single devices a secure and conflict-free operation
is mandatory and containerization is a proven solution. The platform
must enable to provision all these different devices with the correct
software installation. This is usually done by providing a common
endpoint to all devices. Then, a basic setup of the devices is
performed. Example actions are installing the operating system,
provisioning of applications, and providing security credentials.

Zero Touch provisioning concepts are required to support device rollout
by non-it trained personell.

Proposed Standards like [FIDO](https://fidoalliance.org/specifications/)
Device Onboard Specification (FDO) need to be considered for security
(esp. In areas where the physical security of the device can be easily
compromised).

### Configure devices

The onboarded and provisioned devices need to be configured to fulfil
their dedicated roles. Therefore, a use case specific configuration must
be managed by the platform and rollout to the devices on predefined
trigger conditions. For some use cases defining the correct
configuration is an iterative process which needs a corresponding
fine-tuning phase. The platform must enable this iterative process while
always keeping and updating the master configuration without device
specific deviations.

Continually compares current state with desired state. If deviations
occur, a state update is sent down to the device. State updates can be
security or policy updates, changed configurations, firmware / operating
system / application versions (containers).

### Retire devices

Before devices can be decommissioned their retirement has to be planned.
If devices are just being replaced the changeover must be scheduled.
Elimination of devices needs even more planning as the downstream
consequences must be evaluated beforehand. Sometimes unrelated business
processes are dependent on the data the very device is recording and
transmitting. This could be a temperature value of a device equipped to
any machine. It could be used to monitor the environment temperature
while handling the conditioning process of injection molding granulate.
Just shutting down the device would have a negative impact on this
process that is unrelated to the machine itself.

As all technical equipment devices usually contain sensitive data like
keys. This information must be removed before the devices are leaving
corporate property. The platform must keep track of these changes and
document them even after the devices have been removed.


--- <!-- META -->
id: mra-cc-devicemmgt-lifecycle
title: Manage Device Lifecycle
sidebar_label: Manage Device Lifecycle
context: mra-cc > mra-cc-devicemmgt
parent: mra-cc-devicemmgt
child:
prev:
next: mra-cc-devicemmgt-fleets
