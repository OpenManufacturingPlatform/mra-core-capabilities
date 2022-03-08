
## Manage Communication

The de-central structure of manufacturing combined with its mission
critical processes is demanding an asynchronous communication
architecture. This communication is sometimes called store and forward
technique which has its origin in telecommunication. The desired system
behaviour can be established by two different architectures: message
exchange and event streaming. As these architectures are complementary
technologies for different use cases the platform must support both.

Message exchanged is used for a communication when a system requests
another system to complete an action. In most cases the response message
will be processed by the requester. Many existing shop floor applications
are dependent on this communication pattern.

Event streaming is applied for if a system wants to communicate a status
to other enterprise systems. The publish-and-subscribe pattern (Pub/Sub)
is the core mechanism and is reducing the complexity of point-to-point
communication. For some use cases, such as asset tracking, Pub/Sub is
even a prerequisite for economic scaling.

### Provide Messaging

To integrate different applications, message-oriented middleware is a
well-known pattern and solution. It provides capabilities for
communication patterns:
-   point to point
-   pub sub
-   event streaming
-   Persistent / non-persistent,
-   high frequency, low frequency
-   Synchronous / asynchronous

Must support communication types for
-   Telemetry data
-   Command & control
-   Management

This also includes data buffering capabilities, to support offline /
disconnected scenarios. For example, if the wide area connection to the
cloud / core datacenter is lost, telemetry data is buffered in the
streaming component until connection is restored.

### Manage Networks

Ability to manage the many different networks that are required due to
performance and security requirements. Needs to be highly automated,
e.g. use of IT automation tools for firewall configurations etc.
