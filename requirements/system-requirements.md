---
title: System Requirements
desription: >-
  This article discusses the hardware and software requirements that are
  necessary in order to install the SysKit Shell.
author: Andrea Budisa
date: 30/10/2017
---

# System Requirements

## Hardware requirements

**SysKit Shell application and database server**

These are minimum hardware requirements for deploying the **SysKit Shell**, including the deployment of the **Microsoft SQL Server 2012 Express LocalDB**, for a single-server installation or farm installation.

* **Processor:** 2.5 GHz we recommend a processor with at least 4 cores
* **RAM:** 10 GB
* **Disk:** NTFS file system-formatted partition with a minimum of 10 GB of free space
* **Display:** 1366 × 768

{% hint style="warning" %}
Under normal conditions, the application will take around 10 MB of data per server each month for a server, depending on the number of scripts as well as their purpose and result size.
{% endhint %}

## Prerequisites

1. Before installing the SysKit Shell, you need to install **.NET Framework 4.5.2** or later. We recommend that you install the latest version of .NET from the [Microsoft .NET website](https://www.microsoft.com/NET/).
2. SysKit Shell requires **PowerShell version 3.0** or greater to run on a server and to run the scripts on the remote servers.
3. SysKit Shell requires **Windows Management Framework 5.0** or greater to run the PowerShell Gallery cmdlets on the remote servers. [Here you can get](https://www.microsoft.com/en-us/download/details.aspx?id=54616) the latest WMF release.
4. Before starting the installation process, the SysKit Shell installer will automatically perform the installation of **Microsoft Visual C++ Runtime 14.0**.

## Operating System

The SysKit Shell runs on Windows Server 2008 R2 or later. We recommend that you apply all critical updates. You can use the following **Windows Server** editions: **Windows Server 2008 R2 – 2016**, all editions. The SysKit Shell is a 64-bit application that runs on all versions of the above listed operating systems.

## Database System

In order to run the SysKit Shell, you need a database. The SysKit Shell supports **SQL Server databases only**.  
In the installation process, the SysKit Shell Setup will install and configure a new instance of **SQL Server Express 2012 LocalDB** \(free of charge\). This is the quickest option. We take care of the configuration.

> **Learn more about the LocalDB**  
> **LocalDB** is an instance of SQL Server Express that can create and open SQL Server databases. Once LocalDB is installed, the necessary SQL Server infrastructure is automatically created and started, enabling the application to use the database without complex configuration tasks.  
> The system database files for the database are stored in the users’ local AppData path which is normally hidden.  
> For example **C:\ProgramData\SysKit\Shell\SysKitShellDatabase**.

If you want to use SysKit Shell with a dedicated SQL Server located somewhere in your environment, please read [this article.](../how-to/use-dedicated-sql-server.md) It will provide you with detailed instructions on how to perform the transition.  
You can use the following **SQL Server** editions: **SQL Server 2008 – 2016**, all editions. We advise you to use the latest available SQL Server version and apply all the available Service Packs before installing our application.

Proceed to [User Permission Requirements](user-permission-requirements.md)

## Supported technologies and platforms

SysKit Shell supports monitoring of the technologies and platforms listed below.

* **Windows Server** editions: Windows Server 2008 R2 – 2016, all editions
* **SQL Server** editions: SQL Server 2008 – 2016, all editions
* **SharePoint** editions: SharePoint 2013 – 2016, all editions
* Other **Windows Server roles** like **File Server, AD, WSUS, Hyper-V**, etc.

