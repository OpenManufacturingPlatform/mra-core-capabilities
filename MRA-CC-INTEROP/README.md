# Interoperability

A key characteristic of manufacturing is its distributed execution.
Therefore, connecting and integration the different parts of the overall
system are key challenges. The huge amount of legacy production assets
in combination with their specific communication protocols are
increasing the challenges even further.

The following diagram groups the different communication parts into four
areas:

<img alt="Communication Areas" src="/assets/images/INTEROP_commAreas.png" width="25%"/>

According to the OMP IoT Connectivity Whitepaper [\[OMP IOTCON-01
2020\]](https://github.com/OpenManufacturingPlatform/iotcon-connectivity-handbook/tree/publication/White_Paper/01_Insights_Into_Connecting_Industrial_IoT_Assets),
there are three different communication categories: telemetry, control,
and management. Each communication category can occur between all the
areas.

Each area has special aspects to consider, which are described in the
following sub-capabilities:
-   [Connect Assets](ConnectAssets.md)
-   [Integrate Business Systems and Applications](IntegrateSystemsAndApplications.md)
-   [Connect Third Parties](ConnectThirdParties.md)

Sometimes, cardinal points are used to describe the direction of the
connection. That refers to the Purdue / ISA-95 hierarchy (enterprise at
the top, production at the bottom). The following diagram depicts this
from the plant perspective as an example.

<img alt="Communication Directions" src="/assets/images/INTEROP_commDirections.png"
width="50%"/>

As all areas have certain aspects in common, these are grouped into the
following sub-capabilities.
- [Manage Protocols](ManageProtocols.md)
- [Manage APIS and Interfaces](ManageAPIsAndInterfaces.md)
- [Manage Communication](ManageCommunication.md)

Connectivity / integration capabilities have a lot of similarities with
Enterprise Service Bus (ESB) or Enterprise Application Integration (EAI)
architectures. In the OMP context, we expect this to be highly
decentralised and distributed. E.g. the necessary protocol adapters /
transformation capabilities are deployed to where they are needed /
suited best.




--- <!-- META -->
id: mra-cc-interop
title: Interoperability
sidebar_label: Security Overview
context: mra-cc
parent: mra-cc
child: mra-cc-interop-connectAssets
prev: mra-cc-security
next: mra-cc-devicemmgt
