---
title: Install and Configure SysKit Shell
desription: Read this article for detailed step-by-step instructions on how to install the SysKit Shell and all its prerequisites.
author: Andrea Budisa
date: 25/10/2017
---
Before you begin with the SysKit Shell installation, we recommend that you carefully perform all preparation steps by reading the [Pre-Installation Requirements](#internal/) article.

## Installing SysKit Shell

Our application just needs to be installed on a single server, which will then be used for monitoring other servers in the farm.

To install the SysKit Shell, proceed with the following steps:

1. [Download](https://www.syskit.com/products/shell/download) the newest release.
2. Unpack and run the __SysKitShellSetup.exe__. The wizard will guide you through the installation steps; click __Next >__ to proceed.
3. Click __I Accept the terms of the license agreement__ to accept the license and then click __Next >__ to proceed.
4. Select the destination folder for the application installation files, e.g., C:\Program Files\SysKit\Shell. Click __Next >__ to proceed.
5. You can change the folder name where the application shortcuts will be created and modify the availability option to install the SysKit Shell for __All users__ or __Only for the current user__. Click __Next >__ to proceed.
6. In this step you need to enter information about the Service Account that will be used for running the SysKit Shell Service. This account will be used to gather data from your server(s). Enter the custom user account in the following format:
__DOMAIN\USERNAME__.

   > __Please note!__ The service user must be in the local admin group to proceed with this step. For more information about the service account configuration, read the [Add Service User to a Local Administrators Group via Group Policy](#internal/how-to/service-accounts/add-service-user-group-policy) article.

   Click __Next__ to check and validate the credentials.
7. The installation wizard will unpack your files and you will be able to run the application from: __Start > All Programs > SysKit Shell__.

In the installation process, the SysKit Shell Setup will install and configure a new instance of __SQL Server Express 2012 LocalDB__ (free of charge).
This is the quickest option. We take care of the configuration.  

Once the installation is completed, the SysKit Shell will start. If the application does not start automatically after installation, you can run it manually from: __Start > All Programs > SysKit Shell__.

### Problems with Installation and Configuration

Most problems are related to SysKit Shell Service authentication against the Active Directory or the SQL Server instance. If you are experiencing problems with installation, please [contact us](https://www.syskit.com/company/contact-us). Our team will schedule a support call and help you install the SysKit Shell remotely.