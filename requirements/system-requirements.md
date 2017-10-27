---
title: System Requirements
desription: This article discusses the hardware and software requirements that are necessary in order to install the SysKit Shell.
author: Andrea Budisa
date: 25/10/2017
---
## Hardware requirements

__SysKit Shell application and database server__

These are minimum hardware requirements for deploying the __SysKit Shell__, including the deployment of the __Microsoft SQL Server 2012 Express LocalDB__, for a single-server installation or farm installation.

+ __Processor:__ 2.5 GHz; for more than 100 servers, we recommend a processor with at least 4 cores
+ __RAM:__ 4 GB
+ __Disk:__ NTFS file system-formatted partition with a minimum of 500 MB of free space
+ __Display:__ 1366 × 768

> __Please note!__ Under normal conditions, the application will take around 10 MB of data per server each month for a server, depending on the number of scripts as well as their purpose and result size.

## Prerequisites

Before installing the SysKit Shell, you need to install __.NET Framework 4.5.2__ or later. We recommend that you install the latest version of .NET from the [Microsoft .NET website](https://www.microsoft.com/NET/).  
Before starting the installation process, the SysKit Shell installer will automatically perform the installation of __Microsoft Visual C++ Runtime 14.0__.

## Operating System

The SysKit Shell runs on Windows Server 2008 SP2 or later. We recommend that you apply all critical updates.
You can use the following __Windows Server__ editions: __Windows Server 2008 – 2016__, all editions. The SysKit Monitor is a 64-bit application that runs on all versions of the above listed operating systems.

## Database System

In order to run the SysKit Monitor, you need a database. The SysKit Monitor supports __SQL Server databases only__.
You can use the following __SQL Server__ editions: __SQL Server 2008 – 2016__, all editions.
We advise you to use the latest available SQL Server version and apply all the available Service Packs before installing our application.
If you are moving your existing SQL server database to a new SQL server, please follow the instructions in [this article](#internal/how-to/move-database-to-new-server).

See [SQL Permissions](#internal/installation-configuration/configuration-wizard/sql-permissions/create-sql-login) to learn more about SysKit Monitor SQL Server database requirements.

If you __do not have an SQL Server instance__ installed in your server environment, the SysKit Monitor installation will offer to install the __SQL Server Express 2012 LocalDB__ (free license) automatically.

> __Learn more about the LocalDB__   
__LocalDB__ is an instance of SQL Server Express that can create and open SQL Server databases. Once LocalDB is installed, the necessary SQL Server infrastructure is automatically created and started, enabling the application to use the database without complex configuration tasks.  
The system database files for the database are stored in the users’ local AppData path which is normally hidden.  
For example __C:\Users\user\AppData\Local\SysKit Monitor\SysKit_database__.  
User database files are stored where the user designates, typically somewhere in the __C:\Users\user\Documents__ folder.

Proceed to: [User Permission Requirements](#internal/requirements/user-permission-requirements).

## Supported technologies and platforms

SysKit Shell supports monitoring of the technologies and platforms listed below.
+ __Remote Desktop Services__
+ __Windows Server__ editions: Windows Server 2008 – 2016, all editions
+ __SQL Server__ editions: SQL Server 2008 – 2016, all editions
+ __SharePoint__ editions: SharePoint 2007 – 2016, all editions
+ __Microsoft Exchange Server__ editions: Exchange Server 2007 – 2016
+ __Remote Desktop Gateway (RD Gateway) Server__
+ Other __Windows Server roles__ like __File Server, AD, WSUS, Hyper-V__, etc.
+ __Citrix__ editions:
  * MetaframeXP
  * Presentation Server 4.0 and better
  * XenApp 5.0, 6.0, 6.5, 7.5 – 7.11
  * XenDesktop 7.11 App Edition