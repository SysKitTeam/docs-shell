---
title: FAQ
description: This article outlines frequently asked questions regarding the SysKit Shell.
author: Andrea Budisa
date: 25/10/2017
---
### What are SysKit's Shell prerequisites?
+ Supported Windows operating system (all versions) — Windows Server 2008 R2 to Windows 2016.
+ Net Framework 4.5.2 (required only for the server on which you will install SysKit Shell)
+ Microsoft SQL database — the free SQL Server Express 2012 LocalDB is supported.
+ Administrator account that is a member of a local admins security group on all the servers you plan to monitor.

### How long do you store the data?
Data is stored forever by default. Currently, there are no configuration options for the data retention policy in order to save space on the SQL Server.

### What is the back-end database for the software?
We use the SQL Server Express 2012 LocalDB as database backend. All the SQL servers, from Microsoft SQL 2008 to SQL 2016, are supported, but with additional configuration steps which need to be performed manually. 

> __Please note!__ If you want to use SysKit Shell with a dedicated SQL Server located somewhere in your environment, please [read this article](#internal/how-to/use-dedicated-sql-server). It will provide you with detailed instructions on how to perform the transition.

### Do you support different Active Directory domains?
Yes, different domains are supported via the delegated trusts between domains. Our software only requires one-way trust to monitor all the different domains from one central location.

### Do you support delegated administration?
The software does not support different roles for users. You __cannot__ delegate admin permissions (e.g. to a user who can add new servers and administer the application) or the viewer role (e.g. to a user who can only view reports inside the application).

### How you capture data from the remote servers?
SysKit Shell uses agent-less technology to get data from the remote servers. We utilize RDP APIs from Microsoft to get data directly without installing any software on the servers. All the operations are performed by one central SysKit Shell server, and no hardware resources are consumed by the remote servers.

### How I can plan the size of the database?
The software creates around 10 MB of data per monitored server per month. This calculation can vary, depending on the number of scripts as well as their purpose and result size. Therefore, in a case where you have 10 servers, SysKit Shell will generate roughly 10 MB (per server) each month (* 10 servers = 100 MB of data).

### Do I need to restart the server when installing the software?
No, a server restart is not needed.

### How do I add servers for monitoring?
1. Navigate to the __Settings__ screen by clicking on the __Settings__ icon in the left upper corner, and then click the __Servers__ button. 
2. Click the __Add Servers__ button and in the Add Servers wizard, select the servers from the domain(s) and that’s it. The software will connect via the network directly to the servers. It’s as simple as 1-2-3!

### How is the software licensed?
The software requires per user activation, and pursuant to our agreement and terms, only one user may use the subscription. You can activate your license on a __purchased number of servers__ while your subscription is active, meaning that all the servers you wish to activate our product on, need to be licensed. For multiple servers, we offer volume discounts. Please [contact us](https://www.syskit.com/company/contact-us) for a customized quote.

### Do you offer a free trial?
Yes, we offer a [fully featured 30-day trial](https://www.syskit.com/products/shell/download). During those 30 days, you will receive all the support you need with the software. You can easily contact our [support team](https://www.syskit.com/company/contact-us).