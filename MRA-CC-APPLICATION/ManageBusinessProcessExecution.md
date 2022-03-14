## Manage business process execution

There are many approaches to execute business process: workflow
management, rule processing and complex event processing. It is
important that the process implementations are flexible to changes.
Quite too often they are “locked-in” into multiple legacy systems (for
example PLCs) and therefore resistant to change.

The topic can be split into the following aspects
-   Business Rules
-   Business Process Management or Workflow Management

Business Rules and Process have two aspects - a Modeling / Tooling part,
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
externalise the branching conditions of the process flow.

Deviations from planned status are triggering alerts. Some alerts are
handled by system, while others are presented to humans. This human
interaction is typically established by task lists. Experts are in the
lead to take (business) decisions based on the tasked being assigned to
them. A challenge here is the appropriate presentation of these tasks
into the existing working environment.

### Rule Modeling Tools

Externalisation of business rules does need modelling tools. The tooling
needs to support a wide range of personas with different IT background
(“business users”). It can range from simple MIN/MAX value input fields,
via Excel based decision tables and front-end applications to domain
specific languages, and programming languages. There does not need to be
a single central modelling tooling, for different scopes, different
tools, or multiple deployments of the same tools, can be needed.

### Rule Processing

Rule processing is about the externalisation of rules, out of
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

Contains the development / modelling aspect. Tooling (e.g. via web
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
