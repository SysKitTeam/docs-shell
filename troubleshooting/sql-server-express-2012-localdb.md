---
title: SQL Server Express 2012 LocalDB
author: Andrea Budisa
description: This article explains how to troubleshoot issues caused by LocalDB while attempting to access an existing instance using a different username or account.
date: 25/10/17
---
This article is intended for advanced users, administrators, and IT professionals.

If you are using __Microsoft SQL Server 2012 Express LocalDB__ as a database backend with SysKit Monitor, there can be permission issues while attempting to access an existing LocalDB instance using a different username or account. These configuration issues can arise when upgrading the application to a new version and using a different user account.

By default, access to the instance of LocalDB is __limited to its owner__. The data contained in the LocalDB is protected by file system access to the database files.
Ownership of the LocalDB instance __cannot be changed__. It is owned by the user that was used for the configuration.

If you are having connection problems and getting errors while accessing the LocalDB instance, we recommend that you __delete the instance__ owned by the other user and create a new instance under a different user.

> __Please note__! If you want to use a different user account, the existing database cannot be used!

To delete completely the LocalDB instance that is owned by the old user, open __Regedit.exe__ and search for “__SysKitMonitorPrivate__”. You will get two results in total:

1. ‘Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Microsoft SQL Server Local DB\Shared Instances\SysKit Monitor’

2. ‘Computer\HKEY_USERS\ … \SOFTWARE\Microsoft\Microsoft SQL Server\UserInstances\{ … }’

Next, right-click the selected entry and click __Delete__. Then select F3 to find the last entry and __delete__ it like the previous one.

Afterwards, start the Command Prompt as an administrator and perform the following steps to create and manage a __new LocalDB instance__:

1. __sqllocaldb create “SysKitMonitorPrivate”__ – creates a new of instance of SQL Server Express LocalDB.
2. __sqllocaldb share “SysKitMonitorPrivate” “.\SysKitMonitor”__ – shares the specified private instance of LocalDB using the specified shared name.
3. __sqllocaldb start “SysKitMonitorPrivate”__ – starts the specified instance of SQL Server Express LocalDB.

The newly created LocalDB instance should be up and running now and ready for use in the __SysKit Monitor Configuration Wizard__.
If you are having trouble accessing the instance, check its status by entering the following command: sqllocaldb info “SysKitMonitorPrivate”.