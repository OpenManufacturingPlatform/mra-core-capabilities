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

Place workload (containerised or virtualised) to where it is needed and
where enough resources are available, manage the available
compute/network/storage resource at the specific location. The different
non-functional requirements of workloads (e.g. high availability,
disaster recovery, failover, scalability, low latency) must be
supported.

Cloud like, next to self-service IaaS and PaaS services for
-   compute (virtualised and containerised)
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

In larger organisation, charge back of consumed service to cost centers
is required. Esp. If cloud like models are used. Charge back relies on
monitoring data and is integrated with ER

Holistic monitoring of IT service consumption is still in a nascent
state. In larger organisations consumption is typically measured with
hardware usage and being charged to the respective cost centers. To
enable a data-driven enterprise data and service consumption the
platform must monitor and document this. This information is the basis
for (virtual) revenue streams that will be credited to the providers of
the data and services. Some companies are already integrating (external)
monetarisation services into their platforms to incentives the intended
transformation to a data-driven enterprise.

In addition, consumption monitoring is a key capability for sustainable
IT. The knowledge of consumption is the essential foundation for
important decisions like application retirement or cloud migration.
