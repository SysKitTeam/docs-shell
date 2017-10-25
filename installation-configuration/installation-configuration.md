---
title: Install and Configure SysKit Shell
desription: Read this article for detailed step-by-step instructions on how to install the SysKit Shell and all its prerequisites.
author: Andrea Budisa
date: 25/10/2017
---
Before you begin with the SysKit Shell installation, we recommend that you carefully perform all preparation steps by reading the [Pre-Installation Requirements](#internal/) article.

## Installing SysKit Monitor

Our application just needs to be installed on a single server, which will then be used for monitoring other servers in the farm.

To install the SysKit Monitor, proceed with the following steps:

1. [Download](https://www.syskit.com/products/monitor/download) the newest release.
2. Unpack and run the __SysKitMonitorSetup.exe__. The wizard will guide you through the installation steps; click __Next >__ to proceed.
3. Click __I Accept the terms of the license agreement__ to accept the license and then click __Next >__ to proceed.
4. This step allows you to choose the program features that you want to install and change how a feature is installed. The default option is set to install the __SysKit desktop application__ only, but you can choose to install __both__ the __desktop__ and the __web__ feature. Before proceeding, please read the [System Requirements](#internal/requirements/system-requirements). Click __Next >__ to proceed.
5. Select the destination folder for the application installation files, e.g., C:\Program Files\SysKit\Monitor. Click __Next >__ to proceed.
6. You can change the folder name where the application shortcuts will be created and modify the availability option to install the SysKit for __All users__ or __Only for the current user__. Click __Next >__ to proceed.
7. The following step about the installation method will appear if you don’t have a Microsoft SQL Server instance on this particular machine.  
The __Quick Install__ option is recommended in cases where you have from 10 to a maximum of 20 servers. It is the quickest option. We take care of the configuration.  
If you have more than 20 servers and a dedicated SQL server, we advise you to select __Advanced Install__.
You can choose to connect SysKit Monitor with a SQL Server instance you have or you can let the SysKit Setup install a new instance of __SQL Server Express 2012 LocalDB__ (free of charge).
8. The installation wizard will unpack your files and you will be able to run the application from: __Start > All Programs > SysKit Monitor__.


Once the installation is completed, the Configuration Wizard will start. If the wizard does not start automatically after installation, you can run it manually from: __Start > All Programs > SysKit Monitor > Configuration Wizard__.

Proceed to: [Configuration Wizard](#internal/).