---
title: User Permission Requirements
desription: >-
  This article discusses the necessary Service Account you need in order to run
  the SysKit Shell in various environments and describes deployment scenarios
  that affect account requirements.
author: Andrea Budisa
date: 30/10/2017
---

# User Permission Requirements

Please read this article before choosing your service account.

You can configure SysKit Shell to run under designated domain account or local user on a particular computer. When prompted for the Service Account under **SysKit Shell Service credentials**, enter a dedicated **service user**. It must have the proper permission to collect the required activity data and proper privileges to store data to your database.

> **Please note!** As a best practice, we recommend setting a service user that is in the Administrators or Domain Admins group.

We recommend using the **domain account** as the service account. In order for the account to be eligible for running the SysKit Shell service, it must have administrative privileges and must have the[ **Logon as a service**](../how-to/service-accounts/add-service-user-group-policy.md#set-logon-as-a-service-user-for-the-syskit-shell-service-user) permission.

## Account setup

* **Service Account:** Domain account
* **Setup User Account:**
  * This account must be a member of the **Local Administrators** security group on each server you plan to monitor.
  * It must have the **Logon as a service** permissions defined on a domain level.

This is the **recommended** method for most scenarios.

There are two ways to add a service user to the Local Administrators security group. You can configure this [manually](../how-to/service-accounts/add-service-user-manually.md) or via [Group Policy](../how-to/service-accounts/add-service-user-group-policy.md#add-service-user-to-local-administrators-security-group-through-restricted-groups).

## SQL Server setup

* SysKit Shell is using the Windows Authentication to access the database – the service user will be used for authentication on the SQL LocalDB instance.

> **Learn more about the LocalDB**  
> **LocalDB** is an instance of SQL Server Express that can create and open SQL Server databases. Once LocalDB is installed, the necessary SQL Server infrastructure is automatically created and started, enabling the application to use the database without complex configuration tasks.  
> The system database files for the database are stored in the users’ local AppData path which is normally hidden.  
> For example **C:\ProgramData\SysKit\Shell\SysKitShellDatabase**.

If you want to use SysKit Shell with a dedicated SQL Server located somewhere in your environment, please[ read this article.](../how-to/use-dedicated-sql-server.md) It will provide you with detailed instructions on how to perform the transition.  
You can use the following **SQL Server** editions: **SQL Server 2008 – 2016**, all editions. We advise you to use the latest available SQL Server version and apply all the available Service Packs before installing our application.



