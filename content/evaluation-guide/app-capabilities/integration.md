---
title: "Integration"
seo_title: "Integrations in Mendix - Data Mapping Support, REST & Web Services"
seo_description: "Learn how simple it is to integrate with Mendix through REST API, SOAP Web Services & OData as well as how the platform supports data mapping."
category: "App Capabilities"
notoc: true
menu_order: 30
bg: "integration"
tags: ["integration", "data mapping", "rest service", "web service"]
---

Mendix supports connections to other apps and services through industry-standard interfaces and protocols such as REST, SOAP, JDBC, and OData. The platform offers many solutions for ensuring that new applications can both consume and expose data and services in heterogeneous environments.

{{% image_container width="400" %}}
![Mendix Integrations - JSON, REST, SOAP, OData](attachments/integration-overview.png)
{{% /image_container %}}

## How Can I Integrate with Mendix? {#integrate}

Connecting applications and services is simple with Mendix. There are several ways that we enable integration, ranging from consuming and exposing REST APIs, SOAP web services, and OData, to implementing connectors that use external SDKs to extend the native toolbox of the Mendix Platform with integrations such as Kafka event streams, Redis, MQTT, Slack, Twitter, and Salesforce. Many connectors already exist in the Mendix App Store/Marketplace, and they can be downloaded for immediate use inside your applications. Alternatively, you can build your own connectors with our Connector Kit.

For more information, see [How Can I Integrate with Mendix?](integration-overview#integrate-with).

## How Does Mendix Support Data Mapping? {#data}

Being able to easily and visually map external data formats to the entities used in your application is an important aspect of integration. Mendix helps you achieve this with its data mapping functionality that automatically maps incoming message structures (such as JSON, WSDL, or XML) in order to create domain models (if desired) and data mappings. Once the message structure is mapped, incoming data can then be transformed (if required) so it can be used inside your application models.

Read on in [How Does Mendix Support Data Mapping?](data-mappings#data-mapping).

## How Does Mendix Support REST & Web Services? {#support}

Mendix makes exposing and consuming REST and web services simple. To consume, map the incoming message responses from the API or service request using JSON or a WSDL, for example. Once mapped, microflow actions allow you to call the desired service from your logic and process the response directly into your app. Exposing your data and logic is also very simple. Using specific microflow actions, you can publish discoverable endpoints for your services, expose an API via a Swagger definition through microflows, or expose entities with a single click as OData resources.

Discover more in [Service Consumption](service-consumption).

## Read More

* [Integration Overview](integration-overview)
* [Data Mappings](data-mappings)
* [Service Consumption](service-consumption)
* [Service Exposure](service-exposure)
* [External Data](external-data)
