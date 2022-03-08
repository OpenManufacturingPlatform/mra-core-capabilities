
## Manage Protocols

Communication protocols define how different system interact within a
network. IT communication protocols like HTTP and MQTT are established.
But to connecting production assets still is a huge endeavour due to
their variety of (legacy) protocol generations like IO-Link, Profinet,
Modbus and OPC-UA. As many older machines cannot be upgraded
economically the protocol selection is a delicate task.

The platform should manage the minimum number of protocols needed. Third
party solutions or custom-built adapters can handle the complexity
outside the platform and therefore are keeping the complexity out of the
core platform itself.

In most cases protocol conversions will be executed on the lowest level
close to the complexity source (e.g., machines from different vendors).
The platform needs to support this southbound protocol mapping close to
the production assets. There might be reasons good reasons to leave the
conversion to upper level (e.g., bandwidth optimisations requiring
payload transformation to a dedicated cloud service). Therefore the
platform must enable a selection of protocol northbound as well.

### Integrate Services

Integration capabilities are all the capabilities which are commonly
referred to as Enterprise Service Bus (ESB) or Enterprise Application
Integration. It includes adapters, protocol conversion, payload
transformation etc. We expect these capabilities not to be implemented
as a central ESB, which could become a bottleneck. Rather, we expect
decentralised deployment of integration capabilities to where they are
needed.

### Implement Protocols

Provide / adapters for all necessary protocols, esp. The ones listed by
the connectivity capabilities.

### Convert Protocols

Provides the capability to convert between different protocols. This
includes both transport and application layer conversion. For example,
to convert from REST@HTTP to XML@JMS, or from OPC-UA@UDP to Kafka@TCP

### Transform Payload

When integrating different services, frequently data structures need to
be transformed, e.g. from REST to XML, or a single field from the source
system needs to be split and mapped to several fields in the target
system
