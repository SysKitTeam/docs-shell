---
title: Use SysKit Shell with a dedicated SQL Server
desription: >-
  This article explains how to use SysKit Shell with a dedicated SQL Server
  database.
author: Andrea Budisa
date: 30/10/2017
---

# Use SysKit Shell with a dedicated SQL Server

If you want to use a dedicated SQL Server database with SysKit Shell, please perform the following steps:

1. `Stop` the **SysKit Shell Service** using Services.msc.
2. Locate the **CreateDatabase.sql** and **InitializeDatabaseObjects.sql** scripts in the installation folder \(it's usually in C:/Program Files/SysKit/Shell/Service/Script Library\).
3. Execute the **CreateDatabase.sql** script using the SQL Server Mangement Studio or use the SQL Server Management Studio to create a new database on the SQL Server.
   * You can copy all contents from the script and execute them in the context of a database using the SQL Server Management Studio.
4. Using the same procedure, execute the **InitializeDatabaseObjects.sql** script on a previously created database.
   * You can copy all contents from the script and execute them in the context of a database using the SQL Server Management Studio.
5. Locate the **%ProgramData%/SysKit/Shell/settings.json** file and change the connection string property inside it. The connection string should be in the following format:

   ```text
   "Server={Dedicated SQL Server}; Initial Catalog={Database Name}; Integrated Security=true;" 
   ```

   Instead of the {Dedicated SQL Server} and {Database Name} properties, enter the SQL Server name and database name accordingly.

6. `Start` the **SysKit Shell Service**.

