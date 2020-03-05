---
title: "UX & Multi-Channel Apps"
seo_title: "Building UX & Multi-Channel Applications with Mendix Low-Code Platform"
seo_description: "Learn how Mendix supports building multi-channel, mobile and native applications & features that ensure superior UX no matter the device being used."
category: "App Capabilities"
menu_order: 10
notoc: true
bg: "ux"
tags: ["mobile app", "native", "native mobile", "hybrid", "react native", "multi-channel", "offline", "ux", "pwa", "progressive"]
seo_video: "ux-multi-channel-apps"
---

The Mendix Platform offers a completely integrated visual development environment for building multi-channel apps. Developers can rapidly build, visualize, and deploy multi-channel apps using the drag-and-drop interfaces of Mendix Studio and Mendix Studio Pro.

Users can build rich front-ends for multi-channel apps (for both web and mobile apps) from a single model that supports reuse and a consistent look and feel. In addition, Mendix’s [Atlas UI](https://atlas.mendix.com/) framework enables users to create beautiful interfaces quickly via a wealth of Mendix UX resources.

Finally, in addition to many standard components, Mendix offers several options for extending the platform via the Mendix front-end and customizing the look and feel of your applications.

{{% youtube WomZYwyydmQ %}}

## How Does Mendix Support Multi-Channel Applications? {#multi}

Mendix provides a single development paradigm for building multi-channel apps. You can build everything from simple responsive user experiences to progressive web apps or complete offline-first native mobile apps with client-side logic and data synchronization.

Both business and IT developers can create multi-channel apps through Mendix's visual drag-and-drop development environment using a single model base and skill set to serve multiple use cases, including mobile back-end as a service (mBaaS).  Consolidating skills, reducing complexity, and accelerating business value with Mendix will help you to meet the demands of today’s highly mobile workforce.

For more information, see [How Does Mendix Support Multi-Channel Applications?](front-end#support-multi-channel).

## How Do Mendix Mobile Apps Work? {#work}

With Mendix, you can develop, deploy, test, and manage mobile applications from a single integrated visual development environment. Mendix supports three type of mobile apps: [native mobile apps](native-mobile-apps), [progressive web apps](progressive-web-apps), and [hybrid mobile apps](hybrid-mobile-apps).

Mendix native mobile apps are truly native and are based on [React Native](https://facebook.github.io/react-native/). This results in fast performance, smooth animations, natural interaction patterns (like swipe gestures), and access to all the native device capabilities. These applications always have an [offline-first architecture](#offline).

You can also build hybrid mobile apps that use the [Cordova](https://cordova.apache.org/) framework to provide access to native mobile device features. Hybrid mobile applications can operate in an online or offline mode.

The Mendix mBaaS provides over-the-air updates that remove the need to redeploy applications to the app stores in order to deploy new or updated functionality. 

For details, see [How Do Mendix Native Mobile Apps Work?](native-mobile-apps#native-mobile-apps-work) and [How Do Mendix Hybrid Mobile Apps Work?](hybrid-mobile-apps#mobile-apps-work).

## How Can I Build an Offline-first Mobile App? {#offline}

The most important point to make here is that you build Mendix offline-first apps with the same tools you use to build online and responsive apps. This helps to consolidate your skills and knowledge of reuse across the deployment landscape. By simply specifying an offline profile inside your app model, the Mendix Platform will automatically manage both the consistency and deployment of those model artifacts that are required to be synchronized to the device to run locally.

In addition, Mendix creates and synchronizes a local SQLite database to persist data between the client and server automatically, requiring no additional skills to manage data movement when on- or offline.

Default Mendix synchronization patterns can be configured and overwritten by custom models, giving the Mendix developer full control of the synchronization in case the default patterns do not suffice.

For more details, go to [How Can I Build an Offline Mobile App?](offline-apps#build-offline).

## Read More

* [Front-End](front-end)
* [UI Design](ui-design)
* [Native Mobile Apps](native-mobile-apps)
* [Hybrid Mobile Apps](hybrid-mobile-apps)
* [Web Apps](web-apps)
* [Offline-first Apps](offline-apps)
