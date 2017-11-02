---
title: User Permission Requirements
desription: This article discusses the necessary Service Account you need in order to run the SysKit Shell in various environments and describes deployment scenarios that affect account requirements.
author: Andrea Budisa
date: 30/10/2017
---
Please read this article before choosing your service account.

You can configure SysKit Shell to run under designated domain account or local user on a particular computer. When prompted for the Service Account under __SysKit Shell Service credentials__, enter a dedicated __service user__. It must have the proper permission to collect the required activity data and proper privileges to store data to your database.

> __Please note!__ As a best practice, we recommend setting a service user that is in the Adminstrators or Domain Admins group.
 
We recommend using the __domain account__ as the service account. In order for the account to be eligible for running the SysKit Shell service, it must have administrative privileges and must have the __[Logon as a service](#internal/how-to/service-accounts/add-service-user-group-policy)__ permission.

### Account setup

+ __Service Account:__ Domain account
+ __Setup User Account:__
  * This account must be a member of the __Local Administrators__ security group on each server you plan to monitor.
  * It must have the __Logon as a service__ permissions defined on a domain level.

This is the __recommended__ method for most scenarios.

There are two ways to add a service user to the Local Administrators security group. You can configure this [manually](#internal/how-to/service-accounts/add-service-user-manually) or via [Group Policy](#internal/how-to/service-accounts/add-service-user-group-policy).


### SQL Server setup

+ SysKit Shell is using the Windows Authentication to access the database – the service user will be used for authentication on the SQL LocalDB instance.

> __Learn more about the LocalDB__   
__LocalDB__ is an instance of SQL Server Express that can create and open SQL Server databases. Once LocalDB is installed, the necessary SQL Server infrastructure is automatically created and started, enabling the application to use the database without complex configuration tasks.  
The system database files for the database are stored in the users’ local AppData path which is normally hidden.  
For example __C:\ProgramData\SysKit\Shell\SysKitShellDatabase__.

If you want to use SysKit Shell with a dedicated SQL Server located somewhere in your environment, please [contact us](https://www.syskit.com/company/contact-us). We will provide you with detailed instructions on how to perform the transition.  
You can use the following __SQL Server__ editions: __SQL Server 2008 – 2016__, all editions.
We advise you to use the latest available SQL Server version and apply all the available Service Packs before installing our application.

Proceed to: [Pre-Installation Requirements](#internal/requirements/pre-installation-requirements).