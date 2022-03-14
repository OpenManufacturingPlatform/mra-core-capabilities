## Integrate Data

The Integrate set of capabilities ensure that systems and their data
can be combined to ensure that all relevant contextual manufacturing
process, asset and event data can be captured and utilized with the
manufacturing platform.

Data integration, also known as data ingestions, is the first step for
making data available. It is the process of loading data from external
systems in a reliable, secure, and extensible manner. This may involve
generic ingest mechanisms as well as pre-build connectors, standards,
and operating models.

As flexibility is key mechanism like schema on read data APIs such as
OData and GraphQL are gaining popularity. As much information in
manufacturing is stored in relational databases de facto APIs like xDBC
and Gremlin are still the most adopted integration mechanisms today.

### Data Ingest

The capability of being able to bring data into the platform from
external systems in a reliable, secure, and extensible manner. This
capability may include generic ingest mechanisms as well as pre-build
connectors, standards and operating models for ingesting data from
known systems and 3<sup>rd</sup> parties.

### Data Integration & APIs

The capability to provide and interoperate with industry standard
integration APIs, schema on read data APIs (such as OData and GraphQL)
and data technology de facto APIs (such as xDBC and Gremlin) within
the data platform.

## Persist Data

The Persist capability allows for data to be collected, retained and
managed within the manufacturing platform.

Storing data is a fundament capability of every platform. The platform
must support these basic data structure types: structured, unstructured,
semi-structured and timeseries data. The latter is gaining much
importance as they are an efficient means to enable insights from
historical data. Emerging paradigms like Lakehouse are combining some
aspects of the different approaches.

Cloud solutions have significantly reduced the cost of data storage.
Nevertheless, a conscious selection of the data to be stored is still
important as the cost of stored data can not only be measured by the
direct storage service cost: Many data lake projects failed as it was
impossible to obtain meaningful information after some time.

Additionally, the speed to gain access to data is an important cost
aspect. Direct access to data is usually 10 times more expensive than to
archived data. Data archiving therefore is key feature to keep cost
under control.

### Structured

Enables the storage, consumption and query of data that has a strictly
defined content model (schema on write) - e.g. relational and graph
databases.

### Unstructured

Enables the storage, consumption and query of data that has no defined
content model (schema on read) - e.g. object stores and filesystems.

### Semi-structured

Enables the storage, consumption and query of data that may have
unstructured or (potentially multiple) structured content models –
e.g. document databases.

### Time Series

Enables the storage, consumption and query of data that is ordered
chronologically (such as events emitted from plant equipment).
