---
title: SQL Server Express 2012 LocalDB
author: Andrea Budisa
description: >-
  This article explains how to troubleshoot issues caused by LocalDB while
  attempting to access an existing instance using a different username or
  account.
date: 25/10/17
---

# sql-server-express-2012-localdb

This article is intended for advanced users, administrators, and IT professionals.

If you are using **Microsoft SQL Server 2012 Express LocalDB** as a database backend with SysKit Shell, there can be permission issues while attempting to access an existing LocalDB instance using a different username or account. These configuration issues can arise when upgrading the application to a new version and using a different user account.

By default, access to the instance of LocalDB is **limited to its owner**. The data contained in the LocalDB is protected by file system access to the database files. Ownership of the LocalDB instance **cannot be changed**. It is owned by the user that was used for the configuration.

If you are having connection problems and getting errors while accessing the LocalDB instance, we recommend that you **delete the instance** owned by the other user and create a new instance under a different user.

> **Please note**! If you want to use a different user account, the existing database cannot be used!

To delete completely the LocalDB instance that is owned by the old user, open **Regedit.exe** and search for “**SysKitShellInstance**”. You will get the following result:

```text
‘Computer\HKEY_USERS\ … \SOFTWARE\Microsoft\Microsoft SQL Server\UserInstances\{ … }’
```

Next, right-click the selected entry and click **Delete**.

Afterwards, start the Command Prompt as an administrator and perform the following steps to create and manage a **new LocalDB instance**:

1. **sqllocaldb create “SysKitShellInstance”** – creates a new of instance of SQL Server Express LocalDB.
2. **sqllocaldb start “SysKitShellInstance”** – starts the specified instance of SQL Server Express LocalDB.

The newly created LocalDB instance should be up and running now and ready for use in the **SysKit Shell**. If you are having trouble accessing the instance, check its status by entering the following command: sqllocaldb info “SysKitShellInstance”.

