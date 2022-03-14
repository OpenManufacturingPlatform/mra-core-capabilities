
# Application Enablement \[Maintainer: Daniel\]

Applications are the only means by which users can experience a
production platform. Applications are turning platform capabilities into
business value based on the use cases implemented. A wide range of
application architectures needs to be supported: from traditional N-tier
architectures to modern micro-services, event driven and low code
architectures.

Most applications are relying on the underlying platform capabilities,
e.g., interoperability for async messaging, data storage or event
processing.

In the complex manufacturing IT landscape professional dependency and
lifecycles management are key elements of the platform.

## Develop Applications

While many manufacturing applications are COTS (like SCADA, MES or WMS)
every plant is additionally more or less depending on custom-built
solutions. These solutions are developed both in-house and from external
partners. In any case the platform must provide a professional
continuous integration (CI) approach to enable this distributed
development approach. This is even more important in regulated
environments.

### Developer Tooling

Tools for developing applications are needed. From traditional tooling
running on the PC of the developer, to cloud based or low code tooling.

### Support Low Code Application Development

Low code application development provides a fast and easy approach for
simple applications like custom inventory management. Experienced
business users can create these (data entry) applications without IT
support. The challenge of this “grass root” approach is keeping these
solutions in a manageable state. If these applications become too
complex, they are much harder to maintain than classical development
approaches. The platform must therefore enable an optional integration
of low code application and provide mechanism to support an low-code to
non-low-code evolution.

### Manage Application Lifecycle

For a more complex application environment, lifecycle tooling to keep
track of requirements, software assest, their dependencies could be
required.

## Deploy Applications

Getting from development to production requires deployment and
configuration management.

###

### Continuus Integration and Deployment (CI/CD)

All IT systems need to be maintained and updated on a regular basis.
Security updates are typically applied once a month, minor updates at
least once a year. IT systems in general and applications specifically
should be updatable without significant downtime e.g., by applying
rolling update techniques. While continuous deployment (CD) is common in
many IT domains by using sophisticated deployment pipelines, within
manufacturing this is yet a challenge for the same reasons listed in the
*Configure application* capability.

As manufacturing systems are cyber-physical, integration testing is a
challenging task. The physical systems must be simulated to verify that
the overall system will behave as intended after the deployment.
Rollback scenarios are important but are only fixing the IT parts. All
physical effects (e.g., products being assembled, parts being produced)
must be ejected from the manufacturing process and being reworked or
scrapped.

Despite these challenges, deployments become highly automated and are
executed with a pushbutton approach executed by human experts. This is
reducing the deployment process from hours to minutes and making sure
that every step is executed as intended without “manual magic”.
Application deployments are quite often being combined with an update of
the underlying IT systems (like network, operating system, or database).
This ensures a consistent IT stack.

### Manage configurations

Configuration management in general and application configuration in
particular is an underestimated task. It is requiring both business
process and technical knowledge. Applications must be adapted to
(changing) business process without negative effects on operations. This
is especially IT maintenance windows are becoming smaller and smaller.
Opposed to other IT domain, where configurations can be verified e.g.
with AB testing approaches, production is demanding a deterministic
approach where the configuration is pre-defined for every product being
produced. The platform should provide a central and generic application
configuration support.

The central configuration repositories can be used to ensure
consistency, but also detect issues like configuration drift. Yet the
decentral structure of manufacturing demands decentral configurations as
well. Only varying configurations enable global manufacturing of
different product using identical IT systems.

IT automation is used to ensure compliance with policies.

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

## Manage business process execution

There are many approaches to execute business process: workflow
management, rule processing and complex event processing. It is
important that the process implementations are flexible to changes.
Quite too often they are “locked-in” into multiple legacy systems (for
example PLCs) and therefore resistant to change.

The topic can be split into the follwing aspects

-   Business Rules

-   Business Process Management or Workflow Management

Busines Rules and Process have two aspects - a Modeling / Tooling part,
and a runtime/processing part. The first is about

Workflow management is still not widely adopted yet in manufacturing
compared to established domains like HR or finance. The business process
should be modelled using standards like BPMN to enable different runtime
execution environments. Like with rules, it externalized business
processes from the applications and makes them more flexible. Things
like approval steps, parallel sequencing of tasks etc. Like business
rules, this breaks down into runtime and modelling aspect. Business
Process can be long running and have a state which needs to be managed
carefully. Business Process heavily rely on Business Rules (“Scrapping
of parts of value \>1000€ need approval by shift manager”), to
externalize the branching conditions of the process flow.

Deviations from planned status are triggering alerts. Some alerts are
handled by system, while others are presented to humans. This human
interaction is typically established by task lists. Experts are in the
lead to take (business) decisions based on the tasked being assigned to
them. A challenge here is the appropriate presentation of these tasks
into the existing working environment.

### Rule Modeling Tools

Externalization of business rules does need modelling tools. The tooling
needs to support a wide range of personas with different IT background
(“business users”). It can range from simple MIN/MAX value input fields,
via Excel based decision tables and front-end applications to domain
specific languages, and programming languages. There does not need to be
a single central modeling tooling, for different scopes, different
tools, or multiple deployments of the same tools, can be needed.

### Rule Processing

Rule processing is about the externalization of rules, out of
programming code. Instead of hard coding rules in a programming
language, the rules are stored out of the code. The code uses the rule
processing service (can be local or remote) to determine next steps /
actions. It enables easy changing of the rules, without changing the
source code. If needed, rules can even be changed at runtime.

### Complex Event Processing

Complex Event Processing (CEP) is based on rules processing, but able to
process more complex information. This can be due to the need of
aggregating different data source or event streams. As changes in data
sources can be seen as particular event streams, CEP is also known as
stream processing. The power of event streaming lies in the real-time
processing of a multitude unrelated events to derive actions. An example
is the handling of machine alerts which are processed differently in the
context of additional conditions like shift breaks or production
capacity levels. Including historical data (e.g., to detect data drifts)
makes CEP even more powerful.

### Model Business Process

Contains the development / modeling aspect. Tooling (e.g. via web
frontend) to allow easy, fast change of the process to implement
required changes. Tooling is used by a wide range of personas with
different IT backgrounds.

### Execute Business Process

Contains the runtime aspect and is responsible of the actual execution
of the process. Waits for events (“Approved by shift operator”) to then
execute the next step of the process (“Scrap part”).

### Manage Task lists

Execution of business processes needs some kind of task list management,
so that a human worker can see a list of tasks / work orders to execute.
“Approve scraping of this batch yes / no - escalate to supervisor”

### Handle Alerts and Notification

Not only during the execution of business processes, but in a lot of
different contexts, alerts and notification can occur that need to be
handled, e.g. with acknowledgment by a human operator, escalation to a
shift supervisor etc.

## Operate Systems and Applications

Manufacturing is demanding a wide range of systems being deployed from
edge to cloud. This is resulting in complex IT operations procedures. IT
operations is only successful if it is in sync with the non-IT systems
and not focussing on the applications only. Therefore, at least part of
the IT operations is quite often part of the manufacturing organization.
The platform therefore must provide constant SLAs for both the OT and IT
domain. Otherwise, parts of the system will be optimized at the expense
of the other (e.g., reliability vs. modifiability).

The combination of IT and business process monitoring is a key success
factory for reliable platform operations. It is helping to understand
the bi-directional influences and dependencies. If problems are
gradually increasing (e.g., throughput of messages) business processes
can adapt accordingly.

While the practice of DevOps is gaining a lot of momentum in other IT
domains, this is still an exception for manufacturing IT. But moving
workloads to the cloud in combination with a decomposition of the
existing rather monolithic applications will change the current
operation procedures as well. Therefore, support for DevOps is a key
platform capability that must be implemented yet and extent to more and
more services.

### Provide Flexible Compute, Network Storage

Place workload (containerized or virtualized) to where it is needed and
where enough resources are available, manage the available
compute/network/storage resource at the specific location. The different
non-functional requirements of workloads (e.g. high availability,
disaster recovery, failover, scalability, low latency) must be
supported.

Cloud like, next to self-service IaaS and PaaS services for

-   compute (virtualized and containerized)

-   network (software defined)

-   storage (file, block and object storage)

Workload should run as close to the core as possible to simplify
management and operations, and as decentral as needed to support
non-function requirements (data governance, data transmission cost,
latency).

### Manage Updates

All systems need to be maintained and updated on a regular basis. Best
practices are for security updates / patch updates to be applied once a
month, minor updates at least once a year. Platforms and applications
should be updatable without significant downtime e.g., by applying
rolling update techniques.

### Manage Configuration

Configuration management in general and application configuration in
particular is an underestimated task. It is requiring both business
process and technical knowledge. Applications must be adapted to
(changing) business process without negative effects on operations. This
is especially IT maintenance windows are becoming smaller and smaller.
Opposed to other IT domain, where configurations can be verified e.g.
with AB testing approaches, production is demanding a deterministic
approach where the configuration is pre-defined for every product being
produced. The platform should provide a central and generic application
configuration support.

The central configuration repositories can be used to ensure
consistency, but also detect issues like configuration drift. Yet the
decentral structure of manufacturing demands decentral configurations as
well. Only varying configurations enable global manufacturing of
different product using identical IT systems.

### IT Automation

One piece of the puzzle to manage complexity is automation. Provisioning
of systems, configuration (esp. Compliance with security policies),
networks / firewall config can be very time consuming. IT automation
concepts and tools help to reduce the effort, while ensuring consistent
management. E.g. all systems are configured automatically on a daily
basis according to security hardening guidelines.

### Monitoring

Monitoring of all involved systems and components is crucial to be able
to react to problems, but also to plan proactively, e.g. regarding
capacity. SLA monitoring is needed, esp. Operation tasks are outsourced.

### Monitor Consumption / Charge Back

In larger organization, charge back of consumed service to cost centers
is required. Esp. If cloud like models are used. Charge back relies on
monitoring data and is integrated with ER

Holistic monitoring of IT service consumption is still in a nascent
state. In larger organizations consumption is typically measured with
hardware usage and being charged to the respective cost centers. To
enable a data-driven enterprise data and service consumption the
platform must monitor and document this. This information is the basis
for (virtual) revenue streams that will be credited to the providers of
the data and services. Some companies are already integrating (external)
monetarization services into their platforms to incentivize the intended
transformation to a data-driven enterprise.

In addition, consumption monitoring is a key capability for sustainable
IT. The knowledge of consumption is the essential foundation for
important decisions like application retirement or cloud migration.
