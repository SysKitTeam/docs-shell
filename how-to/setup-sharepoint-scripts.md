---
title: Setup SharePoint Scripts
desription: >-
  This article provides guidelines on how to setup the SharePoint Scripts within
  SysKit Shell to return the desired results.
author: Andrea Budisa
date: 31/10/2017
---

# setup-sharepoint-scripts

In some cases, a PowerShell script within SysKit Shell may need to access resources outside the remote server machine. This requires the credentials to be delegated to the target machine.

For example, when the data from SharePoint server are retrieved and a dedicated SQL Server instance needs to be accessed.

To setup the SharePoint Scripts within SysKit Shell to return the desired results, please follow these steps:

1. Read the [Configure CredSSP for use with PowerShell in SysKit Shell](../troubleshooting/credssp-for-use-with-powershell.md) article and **execute a set of cmdlets** to enable the CredSSP authentication on a server where the SysKit Shell is installed.
2. Return to the SysKit Shell and **edit** one by one script in the SharePoint category.
3. Select the desired SharePoint script and click the **Edit** button in the left navigation. The **Edit Script** wizard will open. Click **Next** and in **Edit PowerShell** step, enable the **Use CredSSp PowerShell authentication** option.
4. Fill in the **Username** and **Password** fields by reentering the service credentials. The script first needs to be tested on a selected server. SysKit Shell will run it against the server that you specify.
5. Click **Next** to see the results.
6. Go through all the steps in the wizard and click **Finish** to exit. Edit each next script by choosing the option to use the previously entered credentials.
7. When you configure all the SharePoint scripts according to your preferences, you will be able to **manually execute** them on **all** or **specific** servers.

Happy scripting! :\)

