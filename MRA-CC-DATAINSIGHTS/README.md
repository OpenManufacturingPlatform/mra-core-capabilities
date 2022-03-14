# Data Insights and Actions

The Data Insights & Analytics capability ensures that data can be used
effectively by humans and systems within the architecture to achieve key
use cases. The goal is to turn raw data (that is managed and handled by
the Data Foundation capabilities) into actionable insight.

Companies are following different platform strategies here: While some
companies are having dedicated analytics platform being used for a wide
range of domains (like manufacturing, R&D and sales), other companies
are favouring domain specific platforms that are integrating the
analytics capabilities. The capabilities documented here are valid for
both approaches.

Manufacturing is all about closed-loop operations. A great visualization
not triggering appropriate actions is worthless. Therefore, insights
must be efficiently derived from visualizations and lead to actions. The
platform therefore must integrate actions into the control loop.
Typically, this requires (semi-) automatic control flows into the legacy
applications using the Integrate business application capability. In
most cases a human expert will receive the proposal for a specific
action execution and will then act on his own decision. The platform is
handling this by close integration with the Manage process execution
capability.

Triggering actions at the shopfloor level has security implications as
this often requires a north-south communication. As many production
security policies are only supporting the reverse direction the platform
must enable a reliable yet secure communication.


--- <!-- META -->
id: mra-cc-datainsights
title: Data Foundation
sidebar_label: Data Foundation
context: mra-cc
parent: mra-cc
child: mra-cc-datainsights-analyze
prev: mra-cc-datafoundation
next: mra-cc-application
