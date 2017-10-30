---
title: FAQ
description: This article outlines frequently asked questions regarding the SysKit Shell.
author: Andrea Budisa
date: 25/10/2017
---
### What are SysKit's Shell prerequisites?
+ Supported Windows operating system (all versions) — Windows Server 2008 R2 to Windows 2016.
+ Net Framework 4.5.2 (required only for the server on which you will install SysKit Shell)
+ Microsoft SQL database — the free Microsoft SQL LocabDB is supported.
+ Administrator account that is a member of a local admins security group on all the servers you plan to monitor.

### How long do you store the data?
Data is stored forever by default. Currently, you cannot configure the data retention policy to delete the data after one year, for example.

### What is the back-end database for the software?
We use the SQL Server Express 2012 LocalDB as database backend. All the SQL servers, from Microsoft SQL 2008 to SQL 2016, are supported. All the data is saved inside your datacenter, and we do not upload any data to any outside servers.

### Do you support different Active Directory domains?
Yes, different domains are supported via the delegated trusts between domains. Our software only requires one-way trust to monitor all the different domains from one central location.

### Do you support delegated administration?
The software supports different roles for users. You can delegate admin permissions (to a user who can add new servers and administer the application) and the viewer role (to a user who can only view reports inside the application).

### Do you support multi-tenancy?
If you have multiple clients spread between the same or different servers, you can create views and separate logically organized units, different servers, or users to create dedicated reports for different clients.

### How you capture data from the remote servers?
SysKit Shell uses agent-less technology to get data from the remote servers. We utilize RDP APIs from Microsoft to get data directly without installing any software on the servers. All the calculations are performed by one central SysKit Shell server, and no hardware resources are consumed by the remote servers.

### How I can plan the size of the database?
The software creates around 10 MB of data per monitored server per month. This calculation can vary, depending on the number of scripts as well as their purpose and result size. Therefore, in a case where you have 10 servers, SysKit Shell will generate roughly 10 MB (per server) each month (* 10 servers = 100 MB of data).

### Do I need to restart the server when installing the software?
No, a server restart is not needed.

### How do I add servers for monitoring?
Go to the Administration tab and select the Add button from the upper ribbon. Next, select the servers from the domain and that’s it. The software will connect via the network directly to the servers. It’s as simple as 1-2-3!

### How is the software licensed?
The software is licensed per monitored servers, meaning that all the servers you wish to monitor need to be licensed. For multiple servers, we offer volume discounts. Please [contact us](https://www.syskit.com/company/contact-us) for a customized quote.

### Do you offer a free trial?
Yes, we offer a [fully featured 30-day trial](https://www.syskit.com/products/shell/download). During those 30 days, you will receive all the support you need with the software. You can easily contact our [support team](https://www.syskit.com/company/contact-us).