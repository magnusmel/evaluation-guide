---
title: "External Data"
seo_title: "External Data Support in Mendix - Integrated Data, External Databases, Excel, CSV Formats"
seo_description: "Learn how to import and use external data in your Mendix application such as from Excel, SQL databases, and CSV files from the official evaluation guide."
parent: "integration"
menu_order: 50
bg: "integration"
tags: ["data", "excel", "export", "import"]
---

## 1 How Can I Store & Use Integrated Data in My Applications?

When using data acquired through integrations (for example, web services or REST services), you have two options for storing and using the data, which are described below.

### 1.1 Storing in Persistable Entities

This option means that the data is stored in an application database. This is a good option if you want to use the data for a longer period (as in, hours or days), or if you want to share the data with different users of your application. Another reason to store integration data is when the services you depend on are slow or regularly unavailable.

### 1.2 Storing in Memory via Non-Persistable Entities

This option means that only the user session that retrieved the data has access to the data for the duration of their session. This can be a valid option if you need the data for a short period of time and you want to ensure that it is always in sync with the owner of the data (meaning, the service that provided the data).

Mendix's export and import mappings provide support for both persistable and non-persistable entities.

## 2 How Does Mendix Support Direct Access to an External SQL Database? {#external-sql}

The [Database Connector](https://appstore.home.mendix.com/link/app/2888/) available in the Mendix App Store/Marketplace can be used to run SQL actions on any database you are using. The database connector supports queries as well as actions like updates, deletes, and stored procedure calls.

<video controls src="attachments/DragSQLStatement.mp4">VIDEO</video>

The Database Connector works well with relational databases that support JDBC. Some NoSQL databases also include for SQL through JDBC, so for these NoSQL databases, you may also be able to use the Database Connector. Most NoSQL databases also offer connectivity through REST APIs. If this is the case, you can use Mendix's extensive [REST support](service-consumption#consume-rest-api) to use data in these databases.

For Oracle databases, the [Oracle Connector (Beta)](https://appstore.home.mendix.com/link/app/8683/) is available in the Mendix App Store/Marketplace. This is a version of the Database Connector with support for Oracle-specific features like [PL/SQL](http://www.oracle.com/technetwork/database/features/plsql/index.html), [Ref Cursors](https://docs.oracle.com/cd/E17781_01/appdev.112/e18751/procedures_plsql.htm#TDPNG60040), and [user-defined SQL types](https://docs.oracle.com/database/121/ADOBJ/adobjmng.htm#ADOBJ7651). This module will be useful for many Oracle databases used in Oracle Forms and Oracle Designer applications, where most of the data access is handled by table APIs implemented using PL/SQL packages.

## 3 How Can I Import & Export Data from Sources like Excel?

Right out of the box, the [data grid](https://docs.mendix.com/refguide/data-grid) widget enables you to provide an Excel export of the data displayed in a data grid to your application users. For the bulk import or export of data in the Excel format, you can use the following two Mendix App Store/Marketplace modules:

* [Excel Importer](https://appstore.home.mendix.com/link/app/72/) – This module allows you to define templates for the different Excel sheets you want to import. A template defines the data provided in a sheet as well as how it should be mapped and converted to the entities defined in your Mendix application. You can reuse these templates if you regularly upload the same sheets with updated data.
* [Excel Exporter](https://appstore.home.mendix.com/link/app/726/) – This module allows you to define templates for how you want to export data from your Mendix application as an Excel sheet. Using these templates, you can regularly export data in the exact same formatted Excel sheet. For more information, see [How to Use the Excel Exporter](https://docs.mendix.com/howto/integration/using-the-excel-exporter) in the *Mendix Studio Pro How-to's*.

## 4 How Can I Import & Export CSV-Formatted Data?

The [Mendix App Store/Marketplace](https://appstore.home.mendix.com) contains multiple modules that can help you import or export CSV-formatted data:

* [Excel Export](https://appstore.home.mendix.com/link/app/726/Mendix/Excel-exporter) – This module also supports exporting to the CSV format.
* [Flat & Delimited File Import](https://appstore.home.mendix.com/link/app/429/Erwin-'t-Hoen/Flat-&-delimited-file-import) – This module allows you to import flat and delimited files (CSV) from configuration in the runtime only, relieving you of the Java work.
* [Flat & Delimited File Export](https://appstore.home.mendix.com/link/app/432/Erwin-'t-Hoen/Flat-&-Delimited-File-Export) – This module makes exporting fixed length and delimited files (CSV) easy, as it handles all the Java coding and allows you to easily export your data from a microflow.
* [Simple CSV Exporter](https://appstore.home.mendix.com/link/app/1573/Appronto/Simple-CSV-Exporter) – This module is used for exporting to CSV from a microflow.
* [CSV Services](https://appstore.home.mendix.com/link/app/1911/Mendix/CsvServices) – This module is the easiest and fastest way to get Excel data in and out of Mendix applications. It creates a REST endpoint for every entity in your application, allowing you to upload and download data in comma-separated values format. It also provides microflow actions for importing and exporting CSV in microflows.

### 4.1 How Can I Import & Export Fixed-Length & Delimited Files? {#fixed-length}

Some of the modules above support fixed-length and delimited files.

If you cannot find a module with support for your specific fixed-length format, using the [Mendix Connector Kit](https://www.mendix.com/blog/introducing-mendix-connector-kit/) to create a custom microflow action to handle import and export may be an option. For more info on the Connector Kit and Mendix Java APIs to provide microflow extensions, see the section [How Can I Extend the Functionality of the Mendix Platform?](../enterprise-capabilities/extensibility#extend-functionality) in *Extensibility*.

## 5 How Can I Mass Export & Import? {#mass-export-and-import}

There are a number of ways you can mass export and import data from your Mendix applications:

* **Custom build services** – Examples of this are using web services or REST services. The benefit of this approach is that it enables you to adapt the data and validate it complies with your business rules.
* **Backup and restore** – You can use custom (SQL) scripts to fill a Mendix development database with the data you need. When done, you create a backup of this database and restore it in the desired destination database.
* **Source database** – When you start a runtime on a new empty database, you can specify that it needs to be initialized with data from another database.

If you want to create a real-time mass synchronization between two environments, you can use entity event listeners. This enables you to run custom Java logic for every object event (for example, when data is changed in your database). In this custom handler, you can provide logic to duplicate the data changes to another app.
