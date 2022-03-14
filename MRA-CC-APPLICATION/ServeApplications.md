## Serve Applications

Applications play an important role, as they implement use cases, thus
providing the actual business value. We see three different types of
applications:

### Serve Front-End

Applications which required human interaction. A lot of different
interaction technologies, from traditional PC, via Industrial HMI Touch
Display (usable with gloves), Voice Command, Tablets, Mobile Phone to
Augmented Reality is imaginable. The majority will be more traditional
web-based or rich client like solutions. Front-End Applications have
special requirements regarding usability, authentication & authorization
which need to be considered. A wide range of different personas with
different IT backgrounds and skill levels need to be supported.

### Serve Backend

Backend-Application provide the heavy lifting. Here is where the actual
business logic and algorithms take place. They will probably rely on
capabilities from the data platform. Front-End applications consume
backend applications via APIs.

### Serve Control Loop

Control Loop Applications are really close to operational level. They
control critical parts of the manufacturing process using open or closed
feedback loops from sensors to actuators. Think PLC and SCADA type of
functionality, but software defined. Control Loop Applications can have
demanding requirements regarding availability and latency. Example a
software defined PLC with sub-millisecond latency requirements. Brings
also special security requirements required for command execution to
devices. Depending on the type of devices, safety criticality and
corresponding certifications can be required.
