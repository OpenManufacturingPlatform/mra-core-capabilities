## Compute Data

The Compute capability encompasses all capabilities relating to the
manipulation and mutation of data within the manufacturing platform.
Some of these capabilities might be layered on top of into the
connectivity capabilities of the platform, e.g. data transformation,
enrichment and filtering.

Data processing is encompassing all actions of data manipulation and
mutation. It is executed at different locations. High-frequency data at
the edge level is typically filtered, aggregated and sometimes
compressed before being sent to the cloud. Specialized hardware can be
used in central locations to parallelize computing and thus drastically
required execution times. Data processing or computation therefore is a
key feature of the platform.

An important design decision is the application of batch and stream
processing. Batch processing is concerned with allowing bounded datasets
to be incorporated into the platform (e.g., large, periodic diagnostic
or log file transfer). Stream processing (sometimes called event
processing) is concerned with allowing data in motion to be ingested
(e.g., unbounded streams of data such as status events being emitted
from plant equipment). A typical example is the processing of data from
its data source (e.g., plant equipment) to a sink (e.g., a time series
store), maybe with intermediate processing (aggregation, filtering).
Stateful processing should be avoided but can be needed.

So-called data pipelines are composable and reusable building blocks.
They structure the data transformation process according to the
underlying business rules. Examples of data pipelines are those that may
transform, enrich, conform, or project data into different data
products.

Data processing is often executed on messages in the context of event
driven architectures. Thus, there is most often a tight relationship to
the *Manage messages* capability.

### Stream & Event Processing

Stream and Event Processing is concerned with allowing data in motion
to be ingested (e.g. unbounded streams of data such as status events
being emitted from plant equipment). Typically, connection from a data
source (e.g. plant equipment) to a sink (e.g. a time series store),
maybe with intermediate processing (aggregation, filtering). Stateful
processing should be avoided, but can be needed. Might rely on
Messaging capabilities from Integration Services. These capabilities
might be used by applications that rely on event driven architectures.

### Batch Processing

Batch processing is concerned with allowing bounded dataset(s) to be
incorporated into the platform (e.g. large, periodic diagnostic or log
file transfer).

### Data Pipeline

The data pipeline capability enables the construction of composable
and reusable building blocks of data transformation business rules,
logic and analytics to enable the efficient and consistent delivery of
data products within the platform. Examples of data pipelines are
those that may transform, enrich, conform or project data into
different data products. These pipelines become especially important
when understanding how data can be used from the manufacturing
processes within facilities.

### Edge Data Pre-Processing

Filtering and aggregations of high-frequency data, keep that local to
the edge and sent only relevant data to the cloud. Data can be
pre-filtered or compressed on the edge to avoid massive data upload
from unnecessary data.

### Parallel Compute

Hardware based compute capabilities that are effective for the timely
processing and analysis of data in parallel (e.g. to support Deep and
Machine Learning Capabilities across the manufacturing platform).
