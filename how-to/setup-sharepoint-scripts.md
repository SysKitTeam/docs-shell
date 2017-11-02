---
title: Setup SharePoint Scripts
desription: This article provides guidelines on how to setup the SharePoint Scripts within SysKit Shell to return the desired results.
author: Andrea Budisa
date: 31/10/2017
---
In some cases, a PowerShell script within SysKit Shell may need to access resources outside the remote server machine. This requires the credentials to be delegated to the target machine.

For example, when the data from SharePoint server are retrieved and a dedicated SQL Server instance needs to be accessed.

To setup the SharePoint Scripts within SysKit Shell to return the desired results, follow these steps:

1. Read the [Configure CredSSP for use with PowerShell in SysKit Shell](#internal/troubleshooting/credssp-for-use-with-powershell) article and __execute a set of cmdlets__ to enable the CredSSP authentication on a server where the SysKit Shell is installed.
2. Return to the SysKit Shell app and __edit__ one by one script in the SharePoint category.
3. Select the desired SharePoint script and click the __Edit__ button in the left navigation. The __Edit Script__ wizard will open. Click __Next__ and in __Edit PowerShell__ step, enable the __Use CredSSp PowerShell authentication__ option.
4. Fill in the __Username__ and __Password__ fields by reentering the service credentials. The script first needs to be tested on a selected server. SysKit Shell will run it against the server that you specify.
5. Click __Next__ to see the results.
6. Go through all the steps in the wizard and click __Finish__ to exit. When editing each next script, you will have the option to use the previously entered credentials.
7. When you configure each SharePoint script according to your preferences, you will be able to __manually execute__ them on __all__ or __specific__ servers.