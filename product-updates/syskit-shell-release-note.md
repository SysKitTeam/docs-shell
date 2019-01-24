---
title: SysKit Shell – Document and script all the things!
description: >-
  This article describes all the features and benefits delivered in SysKit
  Shell.
author: Andrea Budisa
date: 2/11/2017
---

# SysKit Shell – Document and script all the things!

We are proud to present our brand new and exciting product **SysKit Shell**! Thanks to our hardworking SysKit team, you can now document and administer your entire Windows-based server environment.

Our development team definitely made a conscious effort in getting big things done and adding a set of very powerful features. Read this release note to discover all the features and benefits!

With our tool you can make **PowerShell Scripts** and import and execute any **script** you can think of! How does it work?

SysKit Shell provides you with a **built-in PowerShell Script wizard** for writing and saving scripts. With this feature, all created PowerShell scripts can be executed with just a few clicks! These scripts can be executed on a number of servers through the **Run** dialog.  
SysKit Shell brings almost **twenty PowerShell scripts** that are ready for you to explore!

If you have no time to write PowerShell Scripts, **PowerShell modules** are quick and easy way to do the task you need!  
SysKit Shell comes with integrated support for browsing and installing modules from **PowerShell Gallery**. With the **Manage modules** feature, you can download a bunch of high quality reusable modules, use them like puzzle pieces and build automation solutions in minutes! Awesome, isn’t it?

We’re always eager to hear your feedback and suggestions!

Product version: 1.0.0  
Build number: 350  
Database version: 1.0.0

Release date: Nov 2, 2017

## SysKit Shell Features

### PowerShell Scripts

* PowerShell Scripts within SysKit Shell are designed to make it as easy as possible for you to take control of and simplify the management of your Windows environments whether you are writing scripts or administering software.
* This section includes **eighteen predefined PowerShell scripts** categorized by their purpose.
* Most of the available PowerShell scripts are tied to a specific server role— such as **Domain Controller** and **SharePoint**, while others can run on all types of servers. It is very important to read the script description.

### PowerShell Wizard

* The **built-in PowerShell Script wizard** brings syntax highlighting and colors to the editor and displays the results of the commands and scripts you have run. One of the key parts of the wizard is PowerShell script error handling, which is the same as in Windows PowerShell.
* Our built-in PowerShell wizard supports **importing** Windows PowerShell scripts with a **.ps1 extension**.
* Wizard has support for the **CredSSP authentication**. In some cases, a PowerShell script may need to access resources outside of the remote server machine. This requires that the credentials be delegated to the target machine.
* Created PowerShell scripts can be tied to a **specific server role** and can be **executed** for all or specific servers.

### PowerShell Modules

* PowerShell modules are a quick and easy way to do a specific task without writing PowerShell Scripts by yourself.
* SysKit Shell has integrated support for browsing and installing modules from the **PowerShell Gallery**.
* You can customize the execution of scripts and cmdlets from modules by supplying your own parameter sets.
* If downloaded modules require **CredSSP** to run their cmdlets or scripts, SysKit Shell will handle that problem for you. All you have to do is supply the credentials.
* If you don't trust an online source, you can always look at the source code by yourself. SysKit Shell will give you a direct link to see the script online before downloading it.
* You don't have to install modules on all the servers where you plan to run them. SysKit Shell will prepare and deploy the files automatically from the server where it is installed.  

  That way the servers you are monitoring do not require internet connection.

### LocalDB

* In the installation process, the SysKit Shell Setup will install and configure a new instance of **SQL Server Express 2012 LocalDB** \(free of charge\).
* It provides the necessary SQL Server infrastructure, enabling the application to use the database without any complex configuration.

## What is the SysKit Shell Licensing model?

* We are introducing the SysKit Shell **Subscription license**. This will allow customers to have usage rights to all releases while their subscriptions are active. 
* The license is tied to an **user account**, it can be purchased **per year**, and is renewable.

