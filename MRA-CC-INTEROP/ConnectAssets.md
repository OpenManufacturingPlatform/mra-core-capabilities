## Connect Assets

Production assets like machines, automated guided vehicles (AGVs) and
equipment are the vital part of each manufacturing plant. To gain
insights about their current state and behaviour the platform must
integrate and connect them to IT systems. This requires the platform to
Manage communication protocols. The required information flow direction
is an important system characteristic: Pushing control and management
information down to the assets (sometimes referred as north-south
communication) is much more challenging than just sending sensor data to
upper IT systems like cloud data storages. Best practices can be derived
by IEC 62443.

However, we also expect modern security architecture and concepts like
zero trust networks to be introduced to production level asset
communication.

Needs to support traditional / specialised / propriety protocols
(Profinet, Powerlink, Modbus, EtherCAT,… ), but also standard / modern
protocols (OPC-UA, MQTT).

Scalability is a key requirement for the platform right from the start.
The approach to connect a 20-year-old brownfield machine will differ
very much from the one to connect 1,000 conveyor belt motors. The
general advice is to analyse, react, filter and aggregate information
flows as early as possible and as late as needed. The scaling stages
must be chosen consciously and align with the overall production network
strategy. The platform must be able to reflect the hierarchical
production structures which are organising the production assets.

As production assets are typically being operated in dedicated and
segmented network environments, setting up bi-directional communication
is still a complex task. Production assets are protected by application
of the Protect resources capability. At scale, this needs to automated
Integrate Business Systems and Applications
