---
title: "Architecture"
seo_title: "Enterprise Architecture Introduction - Twelve-Factor Cloud Native Apps"
seo_description: "Learn more about the Mendix high-productivity aPaaS environment, key architectural principles, components & runtime support for twelve-factor cloud native apps."
category: "Enterprise Capabilities"
menu_order: 10
notoc: true
bg: "architecture"
tags: ["architecture", "model", "statelessness", "twelve factor", "runtime"]
---

Mendix is a high-productivity aPaaS environment built on a modern and open cloud-native architecture for scalability and the freedom to deploy to virtually any infrastructure, including Docker, Kubernetes, and Cloud-Foundry. The platform's stateless server architecture supports on-demand vertical and horizontal scaling, while our public cloud provides self-service scaling and is highly available (HA) by default. Openness and extensibility hooks are available across the platform, from the client and server-side APIs for custom model extensions to the platform APIs and our open-source Model SDK, which allows you to integrate Mendix with your existing tools (CI/CD and DevOps) and build scripts to manage, monitor, and modify the core metadata of your apps.

{{% youtube yR5WA6qHByw %}}

## What Are the Key Architectural Principles Behind the Mendix Platform? {#principles}

The Mendix Platform is architected for the demands of enterprise-ready applications, which are applications that are maintainable, highly performant, and scalable, and can cope with the complex nature of enterprise systems and integration, achieved through the application of the following architectural principles:

* Model-driven development
* Model interpretation over code generation
* Microservices, containers, and deployment standardization
* Statelessness
* Openness and extensibility
* Twelve-Factor App principles

For more information, see [What Are the Key Architectural Principles Behind the Mendix Platform?](architecture-principles#key-principles).

## What Are the Key Components of the Mendix Platform Architecture? {#components}

The Mendix Platform is an integrated application-platform-as-a-service (aPaaS) for the design, build, test, and deployment of enterprise applications. It comprises a sophisticated Developer Portal for app portfolio management, requirements gathering, monitoring, and operations, desktop and web modeling environments for rapid visual app development, and a comprehensive App Store/Marketplace complete with hundreds of reusable components, connectors, and building blocks to accelerate development.

Read on in [What Are the Key Components of the Mendix Platform and Their Architecture?](platform-architecture#key-components).

## How Does the Mendix Runtime Support Twelve-Factor Cloud-Native Apps? {#twelve}

While not strictly a set of architectural principles, the [Twelve-Factor App](https://12factor.net/) methodology is a set of best practices for cloud-native applications covering the following points:

* **Codebase** – one stored codebase and deployments via packages
* **Dependencies** – all dependencies are part of the app model
* **Configuration** – defined in the app model via constraints
* **Backing Services** – configurable at deployment time
* **Build, Release, Run** – separate build and run
* **Processes** - stateless
* **Port Binding** - the app should be self-contained
* **Concurrency** – scale via processes
* **Disposability** - runtime instances can be stopped and started as required
* **Development/Production Parity** – consistent environments across test and production
* **Logs** – collect logs via CF Firehose
* **Admin Processes** – ship the admin and app code in one model

For details about how Mendix applies these factors, see [How Does the Mendix Runtime Support Twelve-Factor Cloud-Native Apps?](twelve-factor-architecture#12-factor).

## Read More

* [Architecture Principles](architecture-principles)
* [Platform Architecture](platform-architecture)
* [Cloud Architecture](cloud-architecture)
* [Runtime Architecture](runtime-architecture)
* [Twelve-Factor Architecture](twelve-factor-architecture)
