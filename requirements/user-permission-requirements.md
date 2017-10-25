---
title: User Permission Requirements
desription: This article discusses the necessary Service Account you need in order to run the SysKit Monitor in various environments and describes deployment scenarios that affect account requirements.
author: Andrea Budisa
date: 25/10/2017
---
Please read this article before choosing your service account.

You can configure SysKit Monitor to run under designated domain account or local user on a particular computer. When prompted for the Service Account under __SysKit Monitor Service credentials__, enter a dedicated __service user__. It must have the proper permission to collect the required activity data and proper privileges to store data to your database.

> __Please note!__ As a best practice, we recommend setting a service user that is in the Adminstrators or Domain Admins group.
 
We recommend using the __domain account__ as the service account. In order for the account to be eligible for running the SysKit Monitor service, it must have administrative privileges and must have the __[Logon as a service](#internal/how-to/service-accounts/add-service-user-group-policy)__ permission.

### Account setup

+ __Service Account:__ Domain account
+ __Setup User Account:__
  * This account must be a member of the __Local Administrators__ security group on each server you plan to monitor.
  * It must have the __Logon as a service__ permissions defined on a domain level.

This is the __recommended__ method for most scenarios.

There are two ways to add a service user to the Local Administrators security group. You can configure this [manually](#internal/how-to/service-accounts/add-service-user-manually) or via [Group Policy](#internal/how-to/service-accounts/add-service-user-group-policy).

> __Please note!__ If the software is installed on a non-domain joined machine, the service account name should be entered in the following form: __machine_name\username__.

### SQL Server setup

+ You can use the Windows Authentication to access the database – the service user will be used for authentication on the SQL Server (recommended).
+ SQL Server Authentication should be used only when Windows Authentication is not possible. This scenario is supported through the SysKit Monitor Configuration Wizard.

If you plan to use Windows authentication, we recommend using our Configuration Wizard to create and configure the SysKit Monitor database. The Active Directory (Windows service) user running the configuration wizard needs to have __dbcreator__ and __securityadmin__ privileges on the SQL Server to create and configure the database.

See [SQL Permissions](#internal/installation-configuration/configuration-wizard/sql-permissions/create-sql-login) to learn more about SysKit SQL server database requirements.   
See [Configure](#internal/get-to-know-syskit-monitor/backstage-screen/configuration/configure) article to learn more on how to change the Service Account or SysKit Monitor database.

Proceed to: [Pre-Installation Requirements](#internal/requirements/pre-installation-requirements).