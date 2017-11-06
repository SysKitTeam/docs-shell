---
title: Use SysKit Shell with a dedicated SQL Server
desription: This article explains how to use SysKit Shell with a dedicated SQL Server database.
author: Andrea Budisa
date: 30/10/2017
---
If you want to use a dedicated SQL Server database with SysKit Shell, please perform the following steps:

1. `Stop` the __SysKit Shell Service__ using Services.msc.
2. Locate the __CreateDatabase.sql__ and __InitializeDatabaseObjects.sql__ scripts in the installation folder (it's usually in C:/Program Files/SysKit/Shell/Service/Script Library).
3. Execute the __CreateDatabase.sql__ script using the SQL Server Mangement Studio or use the SQL Server Management Studio to create a new database on the SQL Server.
   + You can copy all contents from the script and execute them in the context of a database using the SQL Server Management Studio.
4. Using the same procedure, execute the __InitializeDatabaseObjects.sql__ script on a previously created database.
   + You can copy all contents from the script and execute them in the context of a database using the SQL Server Management Studio.
5. Locate the __%ProgramData%/SysKit/Shell/settings.json__ file and change the connection string property inside it. The connection string should be in the following format:

       "Server={Dedicated SQL Server}; Initial Catalog={Database Name}; Integrated Security=true;" 
   Instead of the {Dedicated SQL Server} and {Database Name} properties, enter the SQL Server name and database name accordingly.
6. `Start` the __SysKit Shell Service__.