![OMP Logo](assets/images/omp-logo.png)
# Introduction
The goal of the Manufacturing Reference Architecture (MRA) Working Group
is to provide a fully scalable reference architecture blueprint to
simplify deployment and management of the manufacturing environment.

In this repository, a list of software capabilities that a MRA needs to
provide is presented. Software capabilities are provided by platforms
and applications to implement use cases. See below for a definition and
context on capabilities.

The goal is to provide a repository of capabilities, that can be easily
referenced from the different use cases which rely on the capabilities
and provide more details and context on a certain capability, e.g.
special considerations in manufacturing context.

## Definition of Terms

### Capability

Each use case does require a certain set of capabilities. We will
provide a map of capabilities for each use case. That provides
implementation guidance in regards to:

-   Which capabilities are needed? Helpful e.g. for fit/gap analysis,
    which capabilities are already present, which need to be added.

-   How the capability can be implemented, e.g. using proprietary
    software, open source software, cloud services etc.

-   Special considerations in the manufacturing context, I.e. standards
    that might apply, lessons learned and recommendations.

The following diagram explains the context of software capabilities:

<img alt="ContextDiagramOfCapabilities" src="assets/images/INTRO_contextOfCapabilities.jpg" width="50%" />

As defined in the architecture considerations white paper
\[[OMPMRA01-2020](https://github.com/OpenManufacturingPlatform/MRA-Architectural-Considerations/blob/development/Whitepaper/01_Introduction_to_the_OMP_Manufacturing_Reference_Architecture/02_Approach.md)\],
the capabilities will be provided by a platforms approach as show in the
following figure

<img alt="PlatformApproach" src="assets/images/INTRO_platforms.png" width="50%" />

### Applications

Applications realise use cases using the capabilities of the platform.
Applications can be of all different types like
-   custom developed, maybe using a low code tooling
-   Commercial of the shelf solutions from an ISV
-   Serverless / function as a service snippets
-   Executable machine learning models
-   Apps on a mobile device
-   etc.
There is a many to many relationships between Use Cases and Apps. A
single use case can require multiple applications, a single application
can implement multiple use cases etc. Each application can consume
services / capabilities from all underlying platforms.

### Platforms
The platforms can stretch across the different levels – from the
production level via facility to the enterprise/core. E.g. the data
platform needs to be able to connect to production assets, process high
frequency data at the facility level and send (maybe) aggregated data to
the core level. For consistent operations and management, and to reduce
complexity, it is recommended to use same technology / platforms on all
levels.

<img alt="PlatformAcrossLevels" src="assets/images/INTRO_platformsAcrossLevels.png" width="50%" />

## High Level Structure of core capabilities
Capabilities are grouped into top level categories like “Security” or
“Interoperability”. Each top level category has several “level 2”
capabilities, providing more structure and grouping. The detailed
description is then provided on the lowest level 3. The following
diagram gives an overview by showing only the first two levels.

<img alt="Structure" src="assets/images/INTRO_structureOfCapabilities.png" width="50%" />

## Example Use Case: Condition Monitoring

The following diagram shows on a high level how these capabilities are
used to implement a condition monitoring use case:

<img alt="ExampleUseCase" src="assets/images/INTRO_exampleUseCase.png" width="50%" />

For more details and examples, see the OMP Use Case Collection.

--- <!-- META -->
id: mra-cc-intro
title: Introduction and Overview
sidebar_label: Introduction and Overview
context: mra-cc
parent: mra-cc
prev:
next: mra-cc-security
