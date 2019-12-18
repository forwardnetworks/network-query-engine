
# Network Query Engine (NQE)

Network Query Engine (NQE) by Forward Networks provides information about the network as JSON data in a fully-parsed form.
The information is normalized and presented uniformly across devices from different vendors.
The exported data structures are standards-aligned with [OpenConfig](http://www.openconfig.net/) (details below), and all data is available through a [GraphQL](#graphql) API as well as custom verification checks directly in the Forward Enterprise browser-based interface ([In-App NQE Checks](#in-app-nqe-checks)).

NQE allows network operators to easily build verification checks - for example, to perform sanity checks or to display information - that work across the entire fleet of devices in their network.

This repository helps you get started with NQE.
In particular, it provides information on the [Data Coverage](#data-coverage), the [Relationship to OpenConfig](#open-config) and reference to dedicated GitHub repos with more information about the supported [Interfaces and Examples](#interfaces-examples).

If you'd like to start out with more background on NQE, please check out [this blog post](https://www.forwardnetworks.com/blog/network-query-engine).

<a id="interfaces-examples"></a>
# Interfaces and Examples

There are two ways to consume NQE data, trough the [GraphQL Interface](#graphql) and custom verification checks ([In-APP NQE Checks](#in-app-nqe-checks)).

<a id="graphql"></a>
## GraphQL Interface

The NQE [GraphQL](https://graphql.org/) interface is a simple API that exposes the NQE information as JSON data in a fully-parsed form. This API allows network operators to easily develop scripts and applications in their favorite language or tool that provides a GraphQL client.

![Network Query Explorer](/images/network-query-explorer.png?width=800px&classes=shadow)

The [network-query-engine-examples](https://github.com/forwardnetworks/network-query-engine-examples) repo provides more information on several
GraphQL clients like the [Network Query Explorer](https://fwd.app/network-query-explorer) embedded in Forward Enterprise, [Postman](https://github.com/forwardnetworks/network-query-engine-examples#postman), as well as several  [Python  examples](https://github.com/forwardnetworks/network-query-engine-examples#python-examples).

<a id="in-app-nqe-checks"></a>
## In-App NQE Checks

In-App NQE Checks augments NQE by enabling IT teams to create custom verification checks using the NQE data model, directly in the Forward Enterprise browser-based interface.


![In-App NQE Checks example](/images/in-app-nqe-checks-example.png?width=800px&classes=shadow)

The [in-app-network-query-engine-examples](https://github.com/forwardnetworks/network-query-engine-examples) repo provides more information on several
GraphQL clients like the [Network Query Explorer](https://fwd.app/network-query-explorer) embedded in Forward Enterprise, [Postman](https://github.com/forwardnetworks/network-query-engine-examples#postman), as well as several  [Python  examples](https://github.com/forwardnetworks/network-query-engine-examples#python-examples).

<a id="data-coverage"></a>
# Data Coverage

The initial data set covered by NQE includes:
* Basic device info including device name, vendor, platform, and os.
* Interface data.
* IPv4 and IPv6 RIBs across all VRFs.
* Subset of BGP RIBs (`adj-rib-in` and `adj-rib-out`).
* Topology data via fields that link interfaces to other connected interfaces.

The [Network Query Explorer](https://fwd.app/network-query-explorer) provided by Forward Network instances provides an easy to use tool to interactively view the full schema details.
However, you can also [see the full schema offline here](network-schema.md).

NQE will include more data over time. If the information that you need is not in the schema, please open an issue and request the data.

<a id="open-config"></a>
# Relationship to OpenConfig

Forward Networks NQE is *aligned* with OpenConfig, but is not literally the same data model as any of the various
JSON representations of the OpenConfig YANG data models. Rather, Forward Networks NQE can be seen as an idiomatic
representation of OpenConfig as a GraphQL data source: we have adapted the OpenConfig YANG data models to fit within
the constraints of GraphQL, to adapt to the conventions prevalent within GraphQL APIs, and to take advantage of the
powerful query features available in GraphQL.

Specifically, Forward Networks NQE differs from OpenConfig models in the following ways:
1. Names are camel-cased. Dashes are not permitted in GraphQL.
2. The config and state hierarchy is squashed out, similar to "path-compression" in
[ygot](https://github.com/openconfig/ygot/blob/master/docs/design.md#openconfig-path-compression).
3. OpenConfig sometimes represents some complex entity as a string with specific format, such as vlan range in the
`x..y` format. NQE chooses to model these as structured objects.
4. Some collections of elements, such as BGP routes, are "paged" in NQE because they are often very large. This paging
allows clients to ask for a page of routes at a time.
5. Additional data is sometimes added, such as device platform information under the `platform` field of `Device`, or
the `links` field of an interface that adds topology information to the interface object information.
6. NQE takes advantage of GraphQL's *graph* model to provide fields on objects that link (aka *join*) to related
information. For example, a field of an interface links to other interface to which it is connected. This field
provides the related interface object, not just its name.
7. Forward Networks NQE only covers a subset of OpenConfig models. [More info on included data.](#data-coverage)

# Further reading

* [Product docs](https://app.forwardnetworks.com/docs/docs/applications/network_query_engine/)
* [Network Query Engine Blog Post](https://www.forwardnetworks.com/blog/network-query-engine)
