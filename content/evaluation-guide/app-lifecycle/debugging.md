---
title: "Debugging Facilities"
seo_title: "Application Debugging Tools in Mendix"
seo_description: "Learn how developers can debug any deployed instance of a Mendix app running either locally, on premises, or in the cloud & what debugging tools are available."
parent: "developing-in-mendix"
menu_order: 40
bg: "developing"
tags: ["debug", "cloud", "java", "java action", "eclipse"]
---

## 1 How Can I Debug a Mendix App?

Developers can debug any deployed instance of a Mendix app running either locally, on premises, or in the cloud. Mendix Studio Pro's built-in debugging tools allow it to connect to and authenticate with an app environment using the app instance's URL and the credentials provided from within the Mendix Developer Portal.

<video controls src="attachments/Inspect.mp4">VIDEO</video>

Once connected, the breakpoints defined within microflows will automatically trigger the events that are trapped by Mendix Studio Pro. After triggering, the debugging tool within Mendix Studio and Mendix Studio Pro allows you to step through each microflow action, one action at a time, viewing the changing variables along the route.

For more information about how to use the built-in debugging functionality, see [How to Debug Microflows](https://docs.mendix.com/howto/monitoring-troubleshooting/debug-microflows) in the *Mendix Studio Pro How-to's*.

## 2 How Can I Debug a Live App Running in the Cloud? {#debug-live-app}

The same debugging tools available when debugging locally are available in the cloud. The debugger can be connected to any Mendix app, whether it runs locally, in the cloud, or on premises.

<video controls  src="attachments/debugger.mp4">VIDEO</video>

Read more in [How to Debug Microflows Remotely](https://docs.mendix.com/howto/monitoring-troubleshooting/debug-microflows-remotely) in the *Mendix Studio Pro How-to's*.

## 3 How Can I Debug My Own Custom Java Code in Mendix?

A microflow can be extended with custom Java actions. To make sure these can also be debugged, the Mendix Runtime and Mendix Service Console have been integrated into Eclipse. If you run into an error in any of the Java actions, you can easily debug them utilizing Eclipse's debugger.

When you start the debugger in Eclipse, the full Mendix application is started, and Mendix Studio Pro console logs all the relevant logging information. This makes the debugging experience seamless and fully integrated.

For further information, see [How to Debug Java Actions Remotely](https://docs.mendix.com/howto/monitoring-troubleshooting/debug-java-actions) in the *Mendix Studio Pro How-to's*.
