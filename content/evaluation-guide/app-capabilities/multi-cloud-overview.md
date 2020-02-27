---
title: "Multi-Cloud Overview"
seo_title: "Multi-Cloud Deployment Support - Public, Virtual, & Private Clouds"
seo_description: "Mendix is based on a cloud-native design & Twelve-Factor App principles. Learn more about multi-cloud deployment support, including public, virtual & private clouds."
parent: "deployment"
menu_order: 10
bg: "multicloud"
tags: ["multi cloud", "cloud", "deployment", "on premises", "IaaS", "PaaS"]
---

## 1 What Deployment Options Does Mendix Provide? {#deployment-options}

An application built with Mendix is based on a cloud-native design and conforms to [Twelve-Factor App](https://12factor.net/) principles. The Mendix Runtime is fully optimized to run in a container technology that is compatible with most modern cloud platform offerings like Kubernetes and Cloud Foundry. Mendix apps are thus able to utilize benefits of these cloud platforms such as auto-scaling, auto-provisioning, auto-healing, low infra-overhead, CI/CD support, and cloud interoperability. For more information on these Mendix architecture principles, see [Architecture Principles](../enterprise-capabilities/architecture-principles).

Within this flexible model, Mendix supports a large variety of deployment options that allow you to run your Mendix application on a public, virtual private, private, or hybrid cloud, multi cloud or via a traditional (virtual) server.

{{% image_container width="600" %}}
![Multi-Cloud Infrastructure](attachments/multi-cloud.png)
{{% /image_container %}}

### 1.1 Public Cloud

If you want to acquire the best utilization rate for your infrastructure, to maintain optimal flexibility, and to convert your capital investment into operational expenses, the public cloud is the best choice. Mendix has support for most public cloud vendors, such as Mendix Cloud, IBM, SAP, Microsoft, AWS, and Google. For the Public Cloud - Cloud Foundry providers like Mendix Cloud, SAP, and IBM, we deliver a fully integrated experience in which you can run your app with a single click via your cloud choice.

{{% image_container width="600" %}}
![Multi-Cloud Deployment - IBM, SAP, Azure, AWS](attachments/multi-cloud-deploy.png)
{{% /image_container %}}

For more information, see the section [How Can I Run Mendix in the Public Cloud?](#running-public-cloud) below.

### 1.2 Virtual Private Cloud (VPC)

If your business requires a higher data or application isolation level, a virtual private cloud (VPC) could be the best choice. You still can benefit from a high utilization rate and resource flexibility, but on dedicated hardware or within a separate network segment. A Mendix application runs fully decoupled from our public Mendix Developer Portal, which means running on a VPC can be accommodated easily.

For more information, see the section [How Can I Run Mendix in a Virtual Private Cloud?](#vpc) below.

### 1.3 Private Cloud – On-Premises

If your organization is complying with specific regulations and is not allowed to run in a third-party cloud, you must run your infrastructure on premises. This option can be based on a private cloud or on a traditional server. Mendix can run on both server-based solutions as private cloud infrastructure-as-a-service (IaaS) or platform-as-a-service (PaaS) solutions.

For more information, see the section [How Can I Run Mendix in a Private Cloud or On Premises?](#on-prem) below.

## 2 How Do I Run & Deploy My Mendix Application? {#run-deploy}

In the Mendix Platform, the development and execution of your application are fully separated. After developing the app, you can choose where you want to run it. The sections below explore your deployment options.

### 2.1 How Can I Run Mendix in the Public Cloud? {#running-public-cloud}

Mendix applications can run on all common public cloud providers, like [Mendix Cloud](mendix-cloud-overview.md), Amazon Web Services, Microsoft Azure, IBM Cloud, Google Cloud Platform, SAP Cloud Platform, Redhat Openshift, and Pivotal Web Services.

You can choose the methodology to use – from container-based to VM-based, every methodology is possible.

For more information, see the section [Which Cloud Providers Can I Use for Mendix?](cloud-providers#which-cloud) in *Cloud Providers*.

### 2.2 How Can I Run Mendix in a Virtual Private Cloud? {#vpc}

A virtual private cloud is a public cloud with a dedicated infrastructure like a network, storage, and/or computing allocated to a customer. In most situations, this cloud is only accessible when connected to the customer's network. To run in such a cloud [Mendix Cloud Dedicated](mendix-cloud-overview.md#mendix-cloud-vpc) can be used, or [Mendix for Private Cloud](mendix-for-private-cloud.md#MX4PC). These two options provide a fully opinionated way of running Mendix applications wihtin your VPC.  

This ensures developers maintain the benefit of the one-click deployment experience when using the Mendix Platform in combination with a VPC.

For custom deployment strategies, the Mendix Developer Portal provides a set of APIs that make it possible to configure tools like Jenkins or Microsoft Visual Team services to automate deployment within a VPC. For more information, see [CI/CD](../app-lifecycle/cicd).

### 2.3 How Can I Run Mendix in a Private Cloud or On Premises? {#on-prem}

If you are required to run your software on your own premises, you can choose an infrastructure abstraction level:

* Physical servers
* IaaS
* PaaS

In terms of speed, self-service, and governance, the **PaaS** level has significant benefits. For this reason Kubernetes is the abstraction layer Mendix has adopted as the standard to run Mendix Application in a on-premises scenario. 
For more details see [Mendix for Private Cloud](mendix-for-private-cloud.md#MX4PC)   

Because of the small footprint of a Mendix application, having a two-node (VMs) Kubernetes cluster allows you to run multiple Mendix applications (in multiple environments) with high availability as well as auto-scaling and auto-healing capabilities. 

The use of traditional servers is also still possilbe, but the setup time and maintenance will be significantly higher.

For more information, see the section [Which Operating Systems Do Mendix Studio and Mendix Studio Pro Support?](../app-lifecycle/app-development#operating-systems) in *App Development*.

### 2.4 How Do I Select a Cloud Provider?

Mendix multi-cloud is a deep integration with different cloud providers, which allows you to deploy your application with a single click from Mendix Studio, Mendix Studio Pro, and the Developer Portal.

{{% image_container width="450" %}}
![Deploying Applications to the Cloud](attachments/run.png)
{{% /image_container %}}

The Mendix multi-cloud solution makes use of container-based cloud solutions. The creation of the container and the required services (like the database) is done completely automatically.

It is even possible to switch between cloud providers, so you can start developing and running your application on one cloud and, over time, move it to another cloud.

{{% image_container width="600" %}}
![Selecting a Cloud Platform](attachments/mutli-cloud-selection.png)
{{% /image_container %}}

At the moment, the integrated Mendix multi-cloud solution is provided for Public Cloud Providers: Mendix Cloud, IBM Cloud, and SAP Cloud and (Virtual) Private Cloud providers: Redhat Openshift, Azure AKS, AWS EKS. More clouds will be added to the Mendix multi-cloud portfolio in the near future.

### 2.5 When Should I Use IaaS vs. PaaS?

IaaS is the virtualization of computing, network, and storage running on premises or in the public cloud. A PaaS is an extra abstraction layer on top that allows you to work with services and applications. The abstraction layer of a PaaS will allow you to think in terms of services and applications while providing capabilities like high availability, auto-scaling, auto-healing, auto-provisioning, and user governance.

The choice of either an IaaS or a PaaS in relation to Mendix is based on the amount of applications you are planning to run and who the owner is of the PaaS layer on the cloud.

If you are able to consume a PaaS ondemand from a public cloud, or (Virutal) Private this will always be the best fit for a Mendix hosting solution based on cost, speed, and control.

In the scenario that you have access to an IaaS and you need to choose a PaaS layer yourself (like Kubernetes or Cloud Foundry), the key factor is the number of applications. A Kubernetes cluster can be beneficial when you are planning on running more than two applications, wherein each app contains a test, acceptance, and one or more production environments.  When you are planning on running more than 10 applications, a Cloud Foundry solution could be beneficial (this has to do with the footprint and maintenance of the PaaS layer). Finally, for a single application, a traditional server-based solution will be enough.

## 3 How Can I Run Mendix on a (Virtual) Server or IaaS?

The Mendix Runtime can be directly installed on a server. Mendix provides a service manager for both Linux-based and Windows-based servers that controls the start, stop, and deployment of an application on the server.

{{% image_container width="650" %}}
![Service Console](attachments/mx-service-console.png)
{{% /image_container %}}

For Linux-based applications, this is a command-line based tool called [M2EE](https://github.com/mendix/m2ee-tools).

For details on supported operating systems and related databases, see [System Requirements](https://docs.mendix.com/refguide/system-requirements) in the *Mendix Studio Pro Guide*.

In addition to a container-based solution, Mendix provides full support for a high availability configuration. For more information, see [How to Configure High Availability](https://docs.mendix.com/developerportal/deploy/high-availability) in the Mendix documentation.
