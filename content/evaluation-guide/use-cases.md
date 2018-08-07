---
title: "What Can I Build?"
parent: "introduction"
bg: "mendix"
menu_order: 50
tags: [""]
---

## 1 In General, What Can I Build with Mendix? {#can-i-build}

With Mendix, you can build a wide range of transactional, event-driven, and adjacent applications for all kinds of industries, regardless of complexity, performance, or [scale](enterprise-capabilities/architecture-principles#statelessness).

The [Mendix App Gallery](https://gallery.mendix.com) showcases all kinds of applications built using the Mendix Platform. These applications are there to present you with the art of the possible.

## 2 What Types of Projects Are a Good Fit for Mendix? {#good-fit}

A good way to explain what types of projects are a good fit with Mendix is to segment the type projects by using the Gartner’s [Pace-Layered Model](https://www.gartner.com/binaries/content/assets/events/keywords/applications/apn30/pace-layered-applications-research-report.pdf). Based on this model, an organization’s application landscape is made up of three distinct layers, each with a corresponding rate of change. This rate of change is dictated by the uniqueness of the solutions and how concrete the requirements are.

![](attachments/blog-in-post-pace-payer-model-02.png)

At the bottom of the model is the system of record, which is the foundation of the business. This a structurally solid system with a slow rate of change and well-defined requirements. In the middle is the system of differentiation, which focuses on fostering outside-in and customer-centric thinking, accelerating the rate of change, and developing unique approaches to sustain differentiation. And at the top is the system of innovation, which represents brand new ideas for the organization and thus has fuzzy requirements and a high rate of change.

Mendix helps most in projects where the requirements are not completely defined up front and in projects that have a high rate of change. In line with Gartner’s Pace-Layered Application Strategy, a system of differentiation or innovation matches these criteria. For a system of record, Mendix is a good fit if one of the following points is applicable:

* The application is not available off the shelf
* The off-the-shelf solution is too complex and/or or too expensive
* The customer needs more then 20% customization
* The system of record is also a system of differentiation for the customer
* The customer wants more control over future capabilities

## 3 What Are Common Use Cases for Mendix Applications?

Based on the experience of Mendix's hundreds of enterprise customers, there are four common use cases that are perfect fits for low-code development with Mendix:

* [Innovation apps](#innovation-apps)
* [Customer engagement apps](#customer-engagement-apps)
* [Operational efficiency apps](#operational-efficiency-apps)
* [Legacy migration apps](#legacy-migration-apps)

These four use cases are mapped to Gartner's Pace-Layered Model:

![](attachments/blog-in-post-pace-payer-model-use-cases-03.png)

The sections below describe these use cases in detail.

## 4 How Does Mendix Support Innovation Apps? {#innovation-apps}

Innovation applications stem from ideas for new digital business models, products, and channels to help grow and differentiate an organization. Often, they leverage emerging technologies like IoT, AI, and machine learning to unlock new sources of value. Because innovation apps start as ideas (with loose and fuzzy requirements and a high rate of change), they require a high degree of business involvement throughout the entire development process.

These key platform features enable you to build innovation apps in Mendix:

* [The Mendix Web Modeler](app-lifecycle/app-development#web-modeler) empowers business users to build prototypes that development teams can continue to enhance via the Desktop Modeler.
* [Out-of-the-box connectors](app-lifecycle/app-store#connectors) simplify integration with third-party databases and applications by handling complex XML messages and utilizing IoT and cognitive services. In turn, developers can leverage emerging technologies and legacy systems with minimal dependencies on IT.
* [Requirements management](app-lifecycle/requirements-management) via the easy-to-use [Developer Portal](app-lifecycle/requirements-management#requirements-management) allows business users to create and track their own user stories, enables the development team to adopt a Scrum-based development approach, and shortens the feedback loop between the development team and the business.

Some great examples of innovation apps built with Mendix are AntTail’s [medicine tracking app](https://www.mendix.com/blog/anttail-ensures-quality-medicines-iot/), Solomon Group’s [RFID wristband event access app](https://www.mendix.com/blog/solomon-group-iot-solution/), KLM’s [IoT equipment tracking app](https://www.mendix.com/blog/comes-building-iot-apps-klm-says-just/), and Heijman’s [IoT-based smart building management app](https://www.mendix.com/our-customers/heijmans/).

## 5 How Does Mendix Support Customer Engagement Apps? {#customer-engagement-apps}

Customer engagement applications enable customers and partners to better interact and transact with the business, which helps to improve satisfaction, retention, and revenue. With these apps, the business has a fairly well-defined idea of the app, but the development team must adapt to issues revealed during the application lifecycle. Customer-facing apps often encounter high expectations from unforgiving usage in terms of both usability and seamless, multi-channel access. There are often underlying operational improvements required to support customer-facing processes, and integration with a system of record is required to support the experience layer and existing processes.

These key platform features enable you to build customer engagement apps in Mendix:

* [Multi-channel apps](app-capabilities/ux-multi-channel-apps) can be built once for all channels via the Mendix Modeler's [WYSIWYG page editor](app-lifecycle/user-interfaces#build-pages), which allows users without front-end development or UI design skills to create beautiful, engaging, and highly usable multi-channel apps.
* [The Atlas UI framework](app-capabilities/ui-design#atlas-ui) enables you to build pixel-perfect apps. In addition, your company's UI/UX team can create a package containing the organization’s design language for use across development teams, ensuring consistency while broadly leveraging the skills of what could be a small UI/UX team.
* [Horizontal scalability](enterprise-capabilities/architecture-principles#statelessness) allows additional resources to be added easily as required to support increasing user or processing loads.

Some examples of customer engagement app built with Mendix are agent/broker portals, customer portals, [self-service policy administration apps](https://www.mendix.com/our-customers/texas-life/), claims management apps, and student service applications for universities.

## 6 How Does Mendix Support Operational Efficiency Apps? {#operational-efficiency-apps}

Operational efficiency applications are employee- or partner-facing apps designed to lower costs by reducing or automating manual or paper-based processes. These apps may support departmental, cross-departmental, or company-wide processes, and they are often driven by compliance needs, particularly in regulated industries. This type of app almost always integrates with core systems. The closer the app is to the core systems of the business, the more critical the operational robustness becomes.

These key platform features enable you to build operational efficiency apps in Mendix:

* [The Mendix Web Modeler](app-lifecycle/app-development#web-modeler) empowers business users to build prototypes that development teams can continue to enhance via the Desktop Modeler.
* [Integration options](app-capabilities/integration-overview) are on offer via an extensive array of Mendix tools for integrating with other systems.
* [The Mendix Cloud](app-capabilities/mendix-cloud-overview) enables you to deploy your apps easily and cost-effectively to the cloud.

## 7 How Does Mendix Support Legacy Migration Apps? {#legacy-migration-apps}

Most legacy-migration Mendix application projects are business-driven transformation initiatives. That is, rather than a pure lift-and-shift of existing functionality, these new apps are meant to replace legacy apps that cannot support new processes or provide the right user experience. As such, they require new functionality, but they should also support current processes.

These key platform features enable you to build legacy migration apps in Mendix:

*  [High Availability](enterprise-capabilities/architecture-cloud#cloud-ha) is on offer for all app environments via the Mendix Cloud, ensuring zero downtime in the case of a Mendix Runtime outage.
*  [The Mendix Application Quality Monitor](app-lifecycle/model-consistency#aqm) provides benchmarks in the maintainability of apps based on the ISO 25010 standard, which ensures you are not just building tomorrow's legacy.
*  [Integration options](app-capabilities/integration-overview) are on offer via an extensive array of Mendix tools for integrating with other systems.
*  [Data migration tooling](app-capabilities/querying-managing-data#migrate-from-existing)  is integrated in the Mendix Platform. For example, visual data mapping allows you to create the optimal data model for a new solution (with traceability back to a system of record), rather than simply recreating the legacy system's model.

Some examples of legacy migration apps built with Mendix include apps for transferring legacy [Lotus Notes](https://www.mendix.com/blog/how-one-customer-is-using-mendix-for-legacy-application-migration/), Microsoft Access, SharePoint, or Excel applications to an updated system.

## 8 What Should I *Not* Build in Mendix? {#should-not-build}

While there are endless possibilities for what apps can be built with the platform, we do have some advice on what you should not build in Mendix.

If your application can already be bought off the shelf and provides 100% of the requirements you need, then buying that off-the-shelf product is advised. Buying such a solution is often more cost-effective (based on best practices) and faster to implement. Typically, these off-the-shelf solutions are available for traditional system-of-record applications (which have a low rate of change), because the processes are well established, common to most organizations, and often subject to regulatory requirements. Mendix can extend any application or stay stand-alone.

However, there are situations when the Mendix platform is a good fit even if the app to be built is a traditional system of record. For details on such use cases, refer to [What Types of Projects Are a Good Fit for Mendix?](#good-fit) above.

Finally, the Mendix Platform is not a good fit for building games or replacing full ESB solutions.