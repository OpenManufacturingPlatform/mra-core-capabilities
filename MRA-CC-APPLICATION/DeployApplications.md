## Deploy Applications

Getting from development to production requires deployment and
configuration management.

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
