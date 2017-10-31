---
title: SysKit Shell – Document and script all the things!
description: This article describes all new features, improvements and bug fixes delivered in SysKit Shell.
author: Andrea Budisa
date: 2/11/2017
---

We are proud to present our brand new and exciting product __SysKit Shell__! Thanks to our hardworking SysKit team, you can now document and administer your entire Windows-based server environment.

Our development team definitely made a conscious effort in getting big things done and adding a set of very powerful features. Read this release note to discover all the features and benefits!

With our tool you can make __PowerShell Scripts__ and import and execute any __script__ you can think of! How does it work?

SysKit Shell provides you with a __built-in PowerShell Script wizard__ for writing and saving scripts. With this feature, all created PowerShell scripts can be executed with just a few clicks! These scripts can be executed on a number of servers through the __Run Setup__ dialog.

If you have no time to write PowerShell Scripts, __PowerShell modules__ are quick and easy way to do the task you need!   
SysKit Shell comes with integrated support for browsing and installing modules from __PowerShell Gallery__. With the __Manage modules__ feature, you can download a bunch of high quality reusable modules, use them like puzzle pieces and build automation solutions in minutes! Awesome, isn’t it?

We’re always eager to hear your feedback and suggestions!

[Click here to download the new release.](https://www.syskit.com/products/shell/download)

Product version: 1.0.0  
Build number:   
Database version: 1.0.0

Release date: Nov 2, 2017

### SysKit Shell Features

#### PowerShell Scripts

+ PowerShell Scripts within SysKit Shell are designed to make it as easy as possible for you to take control of and simplify the management of your Windows environments whether you are writing scripts or administering software.
+ This section includes __eighteen predefined PowerShell scripts__ categorized by their purpose.
+ Most of the available PowerShell scripts are tied to a specific server role— such as __Domain Controller__ and __SharePoint__, while others can run on all types of servers. It is very important to read the script description.
+ The __built-in PowerShell Script wizard__ brings syntax highlighting and colors to the editor and displays the results of the commands and scripts you have run. One of the key parts of the wizard is PowerShell script error handling, which is the same as in Windows PowerShell.
+ Our built-in PowerShell wizard supports __importing__ Windows PowerShell scripts with a __.ps1 extension__.
+ Created PowerShell scripts can be tied to a __specific server role__ and can be __executed__ for all or specific servers.

#### PowerShell Modules

+ PowerShell modules are quick and easy way to do the task you need without writing PowerShell Scripts by yourself.
+ SysKit Shell has integrated support for browsing and installing modules from __PowerShell Gallery__.
+ You can customize execution of script and cmdlets from modules by supplying your own parameters sets.
+ If downloaded modules require __CredSSP__ to run their cmdlets or scripts SysKit Shell will handle that problem for you. All you have to do is to supply the credentials.
+ If you don't trust an online source you can always look at the source code by yourself, SysKit Shell will give you a direct link to see the script online before downloading it.
+ You don't have to install modules on all the servers where you plan to run them. SysKit Shell will prepare and deploy the files automatically from the server where it is installed.  
That way the servers you are monitoring do not require internet connection.

#### LocalDB

+ In the installation process, the SysKit Shell Setup will install and configure a new instance of __SQL Server Express 2012 LocalDB__ (free of charge).
+ It provides the necessary SQL Server infrastructure, enabling the application to use the database without any complex configuration.

### What is the SysKit Shell Licensing model?

+ We are introducing the SysKit Shell __Subscription license__. This will allow customers to have usage rights to all releases while their subscriptions are active. The license is tied to an __user account__, it can be purchased __per year__, and is renewable.