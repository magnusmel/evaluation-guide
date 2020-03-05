---
title: "Mendix Cloud Overview"
seo_title: "Mendix Cloud Overview - Architecture, Regions & High Availability"
seo_description: "The Mendix Cloud is built on top of Cloud Foundry & AWS, is available in multiple regions worldwide, & comes with high availability options. Visit for more!"
parent: "deployment"
menu_order: 30
bg: "multicloud"
tags: ["mendix cloud", "high availability", "uptime"]
---

## 1 How Can I Run Mendix on the Mendix Cloud {#mendix-cloud}

The Mendix Cloud is the deployment solution in which Mendix provides hosting environments for customers. The Mendix Cloud is built on top of Cloud Foundry and Amazon Web Services (AWS), is available in multiple regions around the globe, and comes with high availability options. For details on the Mendix Cloud architecture, see [Cloud Architecture](../enterprise-capabilities/cloud-architecture).

Mendix Cloud is the most optimized cloud to run Mendix Applications. It comes standard with deep insights, alerting, high availability, and backups, all of which is self-service available. For more information, see [Mendix Cloud Features](mendix-cloud-features).

## 2 What Does the Mendix Cloud Architecture Look Like?

The Mendix Cloud is a PaaS-based cloud architecture using Cloud Foundry running on top of AWS. A Mendix application runs within fully isolated containers, consuming platform-as-a-service (PaaS) services like databases and storage.

For each region, the Mendix Cloud architecture is set up as fully high-available (HA) and divided into multi-availability zones. This means there is a fully reliable offering for disaster recovery.

{{% image_container width="650" %}}
![Mendix Cloud Architecture Chart](attachments/figure-7-mendix-cloud-deployment-architecture.png)
{{% /image_container %}}

For more information on Mendix Cloud architecture, see [Cloud Architecture](../enterprise-capabilities/cloud-architecture).

## 3 What Mendix Cloud Regions Are Available?

Mendix Cloud is currently available in the following regions:

* US East (North Virginia)
* EU (Frankfurt, Germany)
* EU (Ireland)
* UK (London)
* Japan (Tokyo)

New applications can be placed in any of the available regions. Mendix adds new regions based on customer demand.

![Mendix and Partner Cloud Regions Map](attachments/mx-cloud-regions.png)

## 4 How Does Mendix Cloud support Virtual Private Cloud? {#mendix-cloud-vpc}

Mendix Cloud provides a specific edition to run in the Virtual Private Cloud (VPC) of the customer. This edition is called **Mendix Cloud Dedicated**.

Mendix Cloud Dedicated makes it possible to have a dedicated instance of the Mendix Cloud running on the AWS account of the customer. This instance will consist of a full Mendix Cloud region setup, running within two availability zones of AWS, connected to the private (corporate) network of the customer.   

This instance is still fully managed and operated by Mendix. The user experience and the architecture is identical to **Mendix Cloud Public**. 

![Mendix Cloud Dedicated](attachments/mx-cloud-dedicated.png)

## 5 How Does Mendix Cloud Support High Availability?

Mendix applications consist of five components that are critical for application functionality. These all have to be HA:

* Mendix Runtime
* Database
* File storage service
* HTTPS routing layer
* Network

Because Mendix is hosted on Amazon Web Services (AWS), the file storage service, HTTPS routing layer, and network are HA by default.

The Mendix Runtime supports out-of-the-box horizontal scaling. This allows you to easily scale your application up or down without downtime. In addition, by having at least two instances, you will have a fully high available solution.

For the database, a fallback option needs to be purchased per application where HA is desired. The fallback add-on will enable the Multi-AZ option that AWS RDS offers. When scaling to two or more runtime instances with the fallback option enabled, Mendix applications can be made highly available.

{{% image_container width="500" %}}
![High Availability Infrastructure Chart](attachments/mx-ha.png)
{{% /image_container %}}

For more information, see the sections [How Does Mendix Cloud Offer High Availability?](../enterprise-capabilities/cloud-architecture#cloud-ha), [How Does Mendix Provide Disaster Recovery](../enterprise-capabilities/cloud-architecture#cloud-dr), and [How Does Mendix Cloud Provide Auto-Recovery & Auto-Healing?](../enterprise-capabilities/cloud-architecture#cloud-ar) in *Cloud Architecture*.

## 6 How Does Horizontal & Vertical Scaling Work in the Mendix Cloud?

A Mendix Application relies on these three basic components:

* Mendix Runtime
* Database
* Amazon S3 (file) storage

The Mendix Runtime instances can be scaled horizontally by adding more instances and vertically by adding more memory for each instance. As the Runtime is stateless, no additional effort is needed to run your Mendix app in cluster mode.

By moving a slider in the Mendix Developer Portal, your application will scale up or down without application downtime.

<video controls src="attachments/OA_ScalingEnvironments-1.mp4">VIDEO</video>

For the database, vertical scaling is applied. Because Mendix makes use of standard AWS RDS Postgres instances, it is possible to scale up to a gigantic database with 32 cores and 244 GB of memory.

## 7 How Does Mendix Cloud Support Backup & Recovery? {#support-backup}

Mendix Cloud uses incremental backups with a 15-minute recovery point objective (RPO) for disaster recovery purposes. Nightly backups (with an RPO of 24 hours) are available on a self-service basis. Next to the automatic backups, it is also possible to trigger a backup manually using the Mendix Developer Portal or API.

This video presents how you can create a backup:

<video controls src="attachments/CreateBackup.mp4">VIDEO</video>

For more information, see [Backups](https://docs.mendix.com/developerportal/operate/backups), [How to Create a Backup](https://docs.mendix.com/developerportal/operate/create-backup), and [How to Restore a Backup](https://docs.mendix.com/developerportal/operate/restore-backup) in the *Mendix Developer Portal Guide*.

## 8 What Is the Uptime Guarantee for the Mendix Cloud?

The Mendix Cloud guarantees 99.5% or 99.95% uptime of the cloud infrastructure, depending on your SLA. The 99.95% guarantee only applies to the Mendix Enterprise Edition when the fallback add-on is purchased and the application has been scaled horizontally to two or more instances.

## 9 How Can My App Get Access to My On-Premises Services Without Using a VPN?

The best practice for setting up a secure connection between the Mendix Cloud and your on-premises solution is by using a reverse-proxy with client-server certificates. This allows you to set up a peer-to-peer connection between your application in the cloud and the on-premises solution.

Mendix supports this way of connecting because a VPN comes with significant more maintenance as well as security risk overhead. This is because a VPN will connect to another network not at the application level but at the TCP level. The consequence of this is that, unless you secure your own network with an extra firewall, you are potentially opening your on-premises network to a public network. This is not a best practice and thus not supported by Mendix.

If peer-to-peer integration is not possible because of corporate policies, it is also possible to use Mendix Cloud Dedicated. 

See for more details: [How does Mendix Cloud support Virtual Private Cloud?](#mendix-cloud-vpc)

## 10 How Can the Mendix Support Team Assist Me When Running in the Mendix Cloud?

When approved by the user, [Mendix Support](https://support.mendix.com/hc/en-us) can gain access to the graphs and activity logs of a Mendix Cloud application. For troubleshooting customer tickets, Mendix Support uses this data to more effectively assist users. This is only done with the customer's consent in order to follow specific laws for data privacy.

In addition, Mendix Support utilizes their own experience to advise on app cloud resource pack sizing, performance tuning, app optimization, and more.
