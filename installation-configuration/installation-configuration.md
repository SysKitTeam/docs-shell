---
title: Install and Configure SysKit Shell
desription: >-
  Read this article for detailed step-by-step instructions on how to install the
  SysKit Shell and all its prerequisites.
author: Andrea Budisa
date: 25/10/2017
---

# installation-configuration

Before you begin with the SysKit Shell installation, we recommend that you carefully perform all preparation steps by reading the [Pre-Installation Requirements](installation-configuration.md#internal/requirements/pre-installation-requirements) article.

## Installing SysKit Shell

Our application just needs to be installed on a single server, which will then be used for monitoring other servers in the farm.

To install the SysKit Shell, proceed with the following steps:

1. [Download](https://www.syskit.com/products/shell/download) the newest release.
2. Unpack and run the **SysKitShellSetup.exe**. The wizard will guide you through the installation steps, click **Next &gt;** to proceed.
3. Click **I Accept the terms of the license agreement** to accept the license and then click **Next &gt;** to proceed.
4. Select the destination folder for the application installation files, e.g., C:\Program Files\SysKit\Shell. Click **Next &gt;** to proceed.
5. You can change the folder name where the application shortcuts will be created and modify the availability option to install the SysKit Shell for **All users** or **Only for the current user**. Click **Next &gt;** to proceed.
6. In this step you need to enter information about the Service Account that will be used for running the SysKit Shell Service. This account will be used to gather data from your server\(s\). Enter the custom user account in the following format: **DOMAIN\USERNAME**.

   > **Please note!** The service user must be in the local admin group to proceed with this step. For more information about the service account configuration, read the [Add Service User to a Local Administrators Group via Group Policy](installation-configuration.md#internal/how-to/service-accounts/add-service-user-group-policy) article.

   Click **Next &gt;** to check and validate the credentials.

7. The installation wizard will unpack your files and you will be able to run the application from: **Start &gt; All Programs &gt; SysKit Shell**.

In the installation process, the SysKit Shell Setup will install and configure a new instance of **SQL Server Express 2012 LocalDB** \(free of charge\). This is the quickest option. We take care of the configuration.

Once the installation is completed, the SysKit Shell will start. If the application does not start automatically after installation, you can run it manually from: **Start &gt; All Programs &gt; SysKit Shell**.

## Set-ExecutionPolicy

Before you can explore the UI and run scripts, there is one more thing to do! You need to change the current user preference for the Windows PowerShell execution policy by running the command below.  
Note: Start the Windows PowerShell as the **SysKit Shell service user**.

```text
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy Unrestricted -Force
```

This will let you load all configuration files and run all scripts. If you run an unsigned script that was downloaded from the Internet, you will be prompted for permission before it runs.

### Problems with Installation and Configuration

Most problems are related to SysKit Shell Service authentication against the Active Directory or the SQL Server instance. If you are experiencing problems with installation, please [contact us](https://www.syskit.com/company/contact-us). Our team will schedule a support call and help you install the SysKit Shell remotely.

