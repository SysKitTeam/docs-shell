---
title: Pre-Installation Requirements
desription: This article gives you an overview of the steps you will need to perform in order to prepare your server environment for the SysKit Shell installation.
author: Andrea Budisa
date: 30/10/2017
---
The installation process consists of a few easy steps that you need to perform in order to get the SysKit Shell up and running.

## Configure Active Directory

SysKit Shell requires a service account in order to run. We recommend creating a dedicated Windows account for this purpose.

+ This account needs to have administrative privileges on each server you plan to monitor. You can configure this [manually](#internal/how-to/service-accounts/add-service-user-manually) or via [Group Policy](#internal/how-to/service-accounts/add-service-user-group-policy).
+ This account needs to have the [Logon as a service](#internal/how-to/service-accounts/add-service-user-group-policy) privileges.

> __Please note!__ As a best practice, we recommend setting a service user that is in the Adminstrators or Domain Admins group.

## SQL Server is configured automatically

SysKit Shell Setup will install and configure a new instance of __SQL Server Express 2012 LocalDB__ (free of charge). This is the quickest option. We take care of the configuration.

If you want to use SysKit Shell with a dedicated SQL Server located somewhere in your environment, please [contact us](https://www.syskit.com/company/contact-us). We will provide you with detailed instructions on how to perform the transition.  
You can use the following __SQL Server__ editions: __SQL Server 2008 – 2016__, all editions.
We advise you to use the latest available SQL Server version and apply all the available Service Packs before installing our application.

## Get PowerShellGet Module

PowerShellGet is an in-box module in the following releases:

+ Windows 10 or newer
+ Windows Server 2016 or newer
+ Windows Management Framework (WMF) 5.0 or newer
+ PowerShell 6

### For systems with PowerShell version 3.0 or 4.0 

If you have the PowerShell version 3.0 or 4.0 on a server where you plan to deploy SysKit Shell, you will need to get PowerShellGet module.  
[Download](https://www.microsoft.com/en-us/download/details.aspx?id=51451) the __PackageManagement MSI__ which will enable you to easily discover and install modules and scripts from PowerShell Gallery __using SysKit Shell__.

#### Get the latest version from PowerShell Gallery

Before updating PowerShellGet, you should install the latest __Nuget provider__. To do that, run the following in an elevated PowerShell session:

    powershell Install-PackageProvider Nuget –Force

### For systems running PowerShell 3 or PowerShell 4, that have installed the PackageManagement MSI

Use below PowerShellGet cmdlet from an elevated PowerShell session to save the modules to a local directory: 

    Save-Module PowerShellGet -Path C:\LocalFolder
    Exit

+ Ensure that PowerShellGet and PackageManagment modules are not loaded in any other processes.
+ Delete contents of:

        $env:ProgramFiles\WindowsPowerShell\Modules\PowerShellGet\
        $env:ProgramFiles\WindowsPowerShell\Modules\PackageManagement\ folders.
+ Re-open the PS Console with elevated permissions then run the following commands:

      Copy-Item "C:\LocalFolder\PowerShellGet\*" "$env:ProgramFiles\WindowsPowerShell\Modules\PowerShellGet\" -Recurse -Force
      Copy-Item "C:\LocalFolder\PackageManagement\*" "$env:ProgramFiles\WindowsPowerShell\Modules\PackageManagement\" -Recurse -Force

### For systems with PowerShell 5.0 (or newer) you can install the latest PowerShellGet

To do this on Windows 10, Windows Server 2016, any system with WMF 5.0 or 5.1 installed, or any system with PowerShell 6, run the following commands from an elevated PowerShell session:

    Install-Module –Name PowerShellGet –Force
    Exit

Use Update-Module to get newer versions:

    Update-Module -Name PowerShellGet
    Exit

## Install SysKit Shell

If you have created a service account, and have follwed the above procedure for updating PowerShellGet module and Nuget provider, you can proceed with the SysKit Shell [Installation Wizard](#internal/installation-configuration/installation-configuration).  
In case you haven't followed the steps described above, the SysKit Shell will provide you feedback through informative messages.

If you need help with the installation, please [contact us](https://www.syskit.com/company/contact-us).