---
title: FAQ
description: This article outlines frequently asked questions regarding the SysKit Shell.
author: Andrea Budisa
date: 25/10/2017
---
### What are SysKit's Monitor prerequisites?
+ Supported Windows operating system (all versions)—Windows Server 2008 to Windows 2016.
+ Net Framework 4.5.2 (required only for the server on which you will install SysKit)
+ Microsoft SQL database—the free Microsoft SQL Express is supported.
+ Administrator account that is a member of a local admins security group on all the servers you plan to monitor.

### Can I monitor multiple RDS or Citrix farms from one place?
Yes, SysKit Monitor allows you to monitor multiple farms all from one place. For example, you can combine Windows 2008 with Windows 2012 R2 farms and your old Citrix Presentation Server 4.5 farm with the latest Citrix XenApp 7.6 farm to compare performance on different systems.

### Is XenDesktop supported?
Yes, XenDesktop versions 5.x and higher are supported. All the performance data, including statistics about users and licenses, are available.

### Is VMware Horizon (with View) supported?
Yes, VMware Horizon (with View) is supported with workstations and servers from version 5.x to version 6.x.

### Do you support third-party application publishing software?
Remote application delivery software, such as 2X RAS, Thinspace, Systancia’s AppliDis Fusion, Ericom software, and Propalms, are fully supported.

### Can I schedule reports to be delivered by email?
Yes, you can. All reports inside SysKit Monitor can be scheduled to be delivered by email. We even support saving reports to the network file share or uploading reports to Microsoft SharePoint.

### How long do you store the data?
Data is stored for five years by default. Performance Counters data is stored for 30 days by default due to the large amount of data already collected and newly appearing data. However, you can configure the data retention policy to delete the data after one year, for example.

### What is the back-end database for the software?
We use Microsoft SQL server as does every other Enterprise solution. We do not use Microsoft Reporting Services from the SQL server because we believe that technology is very old, slow, and clumsy. All the SQL servers, from Microsoft SQL 2008 to SQL 2016, are supported. All the data is saved inside your datacenter, and we do not upload any data to any outside servers.

### Do you support different Active Directory domains?
Yes, different domains are supported via the delegated trusts between domains. Our software only requires one-way trust to monitor all the different domains from one central location.

### Do you support delegated administration?
The software supports different roles for users. You can delegate admin permissions (to a user who can add new servers and administer the application) and the viewer role (to a user who can only view reports inside the application).

### Do you support multi-tenancy?
If you have multiple clients spread between the same or different servers, you can create views and separate logically organized units, different servers, or users to create dedicated reports for different clients.

### How you capture data from the remote servers?
SysKit uses agent-less technology to get data from the remote servers. We utilize ICA and RDP APIs from Citrix and Microsoft to get data directly without installing any software on the servers. All the calculations are performed by one central SysKit server, and no hardware resources are consumed by the remote servers.

### How I can plan the size of the database?
The software creates around 40MB of data per monitored server per month. This calculation is based on the assumption that the server hosts approximately 50 users. Therefore, in a case where you have 10 servers, SysKit will generate roughly 40MB (per server) each month (* 10 servers = 400 MB of data).

### Do I need to restart the server when installing the software?
No, a server restart is not needed.

### How do I add servers for monitoring?
Go to the Administration tab and select the Add button from the upper ribbon. Next, select the servers from the domain and that’s it. The software will connect via the network directly to the servers. It’s as simple as 1-2-3!

### How is the software licensed?
The software is licensed per monitored servers, meaning that all the servers you wish to monitor need to be licensed. For multiple servers, we offer volume discounts. Please [contact us](https://www.syskit.com/company/contact-us) for a customized quote.

### Do you support a web-based UI?
Yes, SysKit Monitor comes as an IIS application as well, so you can access it through a web browser.

### Do you offer a free trial?
Yes, we offer a [fully featured 30-day trial](https://www.syskit.com/products/monitor/download). During those 30 days, you will receive all the support you need with the software. You can easily contact our [support team](https://www.syskit.com/company/contact-us).
