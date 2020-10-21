---
title: "Runtime Security"
seo_title: "Mendix Security Model - User Roles, Passwords, Data Level Security"
seo_description: "Learn how application security is defined in Mendix, including defining user roles & password policies, module roles & module-level security, & more!"
parent: "security"
menu_order: 35
bg: "security"
tags: ["runtime security", "runtime", "security", "data layer", "owasp", "multi tenant", "password", "authenticate", "encryption"]
---

## 1 How Is Security Handled in a Mendix App?

Before understanding how security is handled in a Mendix application, it is important to understand the [Mendix Runtime architecture](runtime-architecture).

In a Mendix application, the UI layer is implemented in the Mendix Client as JavaScript libraries running in the browser. For hybrid mobile applications, the UI layer runs in a native Cordova container. The logic and data layers are implemented in the Mendix Runtime (the Mendix Runtime itself is developed in Java and runs on a Java virtual machine).

{{% image_container width="600" %}}
![Runtime Architecture](attachments/mendix-architecture.png)
{{% /image_container %}}

Within the Mendix Client, we implement measures against JavaScript-based security threats such as cross-site scripting. This prevents other websites and web applications running in the same browser from obtaining sensitive information from the Mendix app (for example, cookies).

What is more, the Mendix Runtime addresses server-side security threats, such as SQL injection and code execution. By default, a request originating from any client (including the Mendix Client) is perceived as untrusted.

Mendix app developers do not need to take technical security aspects into consideration when building Mendix apps, as the platform handles this as a service. Of course, this does not mean that developers do not have to consider security at all. Application-level authorization and access rights need to be configured in the application model by the developer. This is because most technical security aspects can be solved generically, while the business rules and requirements that are the prerequisites for access to data can be different for each application and business.

Each operation within the Mendix Runtime is called an “action”. The Mendix Runtime provides many predefined actions, such as triggering and executing workflows and evaluating business rules. To prevent any bypassing of the technical security mechanisms, these actions are implemented at the lowest levels of the Mendix Runtime, and they cannot be changed by app developers.

The core interface of the Mendix Runtime (which is responsible for the execution of any action) has a security matrix that contains all executable actions and data access rules per user role. The data access rules are applied at runtime when a query is sent to the database. This ensures that only data within the boundary of the access rule constraint is retrieved.

## 2 How Does My Mendix App Handle Known Security Threats?

The Mendix Runtime and Mendix Client have out-of-the-box security measures that protect your Mendix applications against known security threats (including, but not limited to, SQL injection, XSS, CSRF, and broken authentication). These security measures undergo monthly external penetration testing. The Mendix Runtime and Mendix Client are scanned daily, using the latest technologies in static analysis and software composition analysis offered by industry leaders, to ensure no unmitigated vulnerabilities remain. This means that, whenever a Mendix application is built solely using a Mendix application development environment, customers do not have to implement static analysis or software composition analysis measures.

## 3 Does My Mendix App Comply with the OWASP Top 10?

The Mendix Runtime protects your application and data according to your model, while the Mendix Cloud handles security at the infrastructural level. The Mendix Runtime takes care of most known security threats (OWASP top 10) out of the box, as the functionality that causes most common security mistakes is abstracted away from developers.

For more information on keeping your Mendix application safe from attackers, see [How to Implement Best Practices for App Security](https://docs.mendix.com/howto/security/best-practices-security) in the *Mendix Studio Pro How-to's*.

## 4 How Is Security Handled at the Application Level?

To provide full security for a Mendix application, you need to explicitly give access to forms, entities, and microflows to a user role. The end-user must have this role before they can access them. By default, no end-user can access anything. To make it easier to create prototypes and demos, there are security levels that require fewer security settings than are needed for a production system.

### 4.1 How Are User Roles Assigned to Users in My App? {#user-roles-assigned}

Based on policy rules, end-users are assigned a user role either within the application, or through the Mendix Developer Portal. MxID (Mendix's end-user management and provisioning service) automatically reads and assigns the user roles defined in the application.

### 4.2 How Is Security Handled at the Mendix Data Layer?

Data security in Mendix is handled by defining the data access rules on your entities. Per entity, you can define who can see what data and who can create or delete data.

{{% image_container width="600" %}}
![Entity Access Rules](attachments/entity_access_rules.png)
{{% /image_container %}}

These rules will be applied every time your application uses an entity. The rules will be applied automatically to XPath retrieves done on your model. You can define XPath constraints on entities, which means you can define access rules depending on the user role or organization. This can be used to ensure strict data separation in multi-tenant applications.

## 5 How Are Permissions Assigned with My App?

Apart from the company profile and settings, Mendix supports the definition of Company Admins who can assign permissions to users following a delegated administration concept. One or more administrators can be identified per tenant who can, in turn, perform administrative tasks in the tenant according to the permissions granted.

## 6 How Are Users & Services Authenticated When Accessing My Mendix App?

The authentication of users and services accessing Mendix apps is handled through MxID by default. MxID applies the OpenID standard.

### 6.1 How Are Passwords Stored in My Mendix App? {#password}

Passwords in Mendix can only be stored in a hashed format. Mendix supports multiple hashing algorithms.

### 6.2 How Does Mendix Support Locking an Account After Failed Login Attempts?

If a user fails to log in with the correct password three times, the user account is blocked automatically for a minimum of 10 minutes.

An administrator can manually override such a block by resetting the password.

### 6.3 How Does Mendix Authenticate System & Service Interfaces Using Web Services, REST Services & APIs?

System and service interfaces must also be authenticated in the context of the attached role. The default option for this is through a username and password, but other options like tokens are also possible. Authorization for APIs is derived from the authorizations defined in the application model.

For authentication, Mendix supports the following technical implementations:

* HTTP authentication
* Web service security standards
* Custom defined authentication mechanisms including Java

These options make it possible to apply identity propagation.

## 7 Which Identity Management Solutions Can I Use in My Mendix App?

Mendix offers MxID as part of Mendix Cloud. MxID is built on the Mendix Platform and thus inherits all security measures from the platform. MxID provides an administration portal for the management of user access and authentication.

## 8 How Does Mendix Support Single Sign-On?

In a multi-app landscape, the value of each application significantly increases when they become interconnected. End-users need to be able to switch between different functionalities (apps) without friction. Application providers have the task of removing that friction. But on an internet that’s populated by people trying to get into accounts for nefarious reasons, end-user authentication is a high-stakes game. It needs to be fast and easy to implement as well as manageable and secure. Insight into usage and interconnectivity levels are also invaluable for improving operations.

Single sign-on (SSO) is a solution. Mendix provides support for SSO standards like SAML 2.0 and OpenID alongside other authentication mechanisms such as two-factor authentication, but building your own solution can prove challenging.

Mendix SSO provides the next generation of user identification on the Mendix platform. Mendix SSO is based on the *OpenID Connect* framework. This enhances the multi-app integration possibilities by using identity propagation. With identity propagation, you can build secure and personalized interfaces between applications, enable fine-grained resource access control for your users, and gain clear usage statistics.

In Mendix Studio, Mendix SSO is automatically configured when you publish an app. This brings the time developers would spend on activating SSO with Mendix accounts in your app down to zero. Simply deploy and invite your users.

## 9 How Does My Mendix App Support Multi-Tenancy?

Mendix offers out-of-the-box support for developing multi-tenant applications. Multi-tenant apps in Mendix share the same database, application logic, and user interface. Application logic can be extended with tenant-specific logic, and the UI can be styled per tenant.

The tenant object is used to do the following:

* Define a **tenant-aware object model** for the application – tenant-level access to domain objects is configured using XPath definitions, which restricts access to those application object instances for the company to which the end-user belongs
* Define **tenant-specific microflows** and configure access rights to implement tenant-level application and process logic
* Apply **tenant-specific styling** of the UI by making the CSS dependent on the companies defined in the MxID

Tenants can be custom defined in the application as well by using identifiers like division, country, and site.

## 10 What Kind of Encryption Is Available in My Mendix App?

Besides the default encryption at rest and in transit, users are able to implement column encryption or uploaded file encryption. Column and uploaded file encryption are supported out of the box via the [Encryption](https://appstore.home.mendix.com/link/app/1011/) module from the Mendix App Store/Marketplace using AES encryption.
