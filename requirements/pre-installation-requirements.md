---
title: Pre-Installation Requirements
desription: >-
  This article gives you an overview of the steps you will need to perform in
  order to prepare your server environment for the SysKit Shell installation.
author: Andrea Budisa
date: 30/10/2017
---

# Pre-Installation Requirements

## Configure Active Directory

SysKit Shell requires a service account in order to run. We recommend creating a dedicated Windows account for this purpose.

* This account needs to have administrative privileges on each server you plan to monitor. You can configure this [manually](../how-to/service-accounts/add-service-user-manually.md) or via [Group Policy](../how-to/service-accounts/add-service-user-group-policy.md).
* This account needs to have the [Logon as a service](../how-to/service-accounts/add-service-user-group-policy.md) privileges.

{% hint style="warning" %}
**Please note!** As a best practice, we recommend setting a service user that is in the Adminstrators or Domain Admins group.
{% endhint %}

## SQL Server is configured automatically

SysKit Shell Setup will install and configure a new instance of **SQL Server Express 2012 LocalDB** \(free of charge\). This is the quickest option. We take care of the configuration.

If you want to use SysKit Shell with a dedicated SQL Server located somewhere in your environment, please [read this article](../how-to/use-dedicated-sql-server.md). It will provide you with detailed instructions on how to perform the transition.  
You can use the following **SQL Server** editions: **SQL Server 2008 – 2016**, all editions. We advise you to use the latest available SQL Server version and apply all the available Service Packs before installing our application.

## Get PowerShellGet Module

PowerShellGet is an in-box module in the following releases:

* Windows 10 or newer
* Windows Server 2016 or newer
* Windows Management Framework \(WMF\) 5.0 or newer
* PowerShell 6

### For systems with PowerShell version 3.0 or 4.0

If you have the PowerShell version 3.0 or 4.0 on a server where you plan to deploy SysKit Shell, you will need to get PowerShellGet module.  
[Download](https://www.microsoft.com/en-us/download/details.aspx?id=51451) the **PackageManagement MSI** which will enable you to easily discover and install modules and scripts from PowerShell Gallery **using SysKit Shell**.

#### Get the latest version from PowerShell Gallery

Before updating PowerShellGet, you should install the latest **Nuget provider**. To do that, run the following in an elevated PowerShell session:

```text
powershell Install-PackageProvider Nuget –Force
```

### For systems running PowerShell 3 or PowerShell 4, that have installed the PackageManagement MSI

Use below PowerShellGet cmdlet from an elevated PowerShell session to save the modules to a local directory:

```text
Save-Module PowerShellGet -Path C:\LocalFolder
Exit
```

* Ensure that PowerShellGet and PackageManagment modules are not loaded in any other processes.
* Delete contents of these folders:

  ```text
    $env:ProgramFiles\WindowsPowerShell\Modules\PowerShellGet\
    $env:ProgramFiles\WindowsPowerShell\Modules\PackageManagement\.
  ```

* Re-open the PS Console with elevated permissions then run the following commands:

  ```text
  Copy-Item "C:\LocalFolder\PowerShellGet\*" "$env:ProgramFiles\WindowsPowerShell\Modules\PowerShellGet\" -Recurse -Force
  Copy-Item "C:\LocalFolder\PackageManagement\*" "$env:ProgramFiles\WindowsPowerShell\Modules\PackageManagement\" -Recurse -Force
  ```

### For systems with PowerShell 5.0 \(or newer\) - install the latest PowerShellGet

To do this on Windows 10, Windows Server 2016, any system with WMF 5.0 or 5.1 installed, or any system with PowerShell 6, run the following commands from an elevated PowerShell session:

```text
Install-Module –Name PowerShellGet –Force
Exit
```

Use Update-Module to get newer versions:

```text
Update-Module -Name PowerShellGet
Exit
```

## Install SysKit Shell

If you have created a service account, and have follwed the above procedure for updating PowerShellGet module and Nuget provider, you can proceed with the SysKit Shell [Installation Wizard](../installation-configuration/installation-configuration.md).  
In case you haven't followed the steps described above, the SysKit Shell will provide you feedback through informative messages.

If you need help with the installation, please [contact us](https://www.syskit.com/company/contact-us).

