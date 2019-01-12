---
title: Configuring CredSSP for use with PowerShell in SysKit Shell
author: Andrea Budisa
description: >-
  This article explains how to enable WSManCredSSP for more advanced PowerShell
  scripts to work in SysKit Shell.
date: 25/10/17
---

# credssp-for-use-with-powershell

Windows Remote Management \(WinRM\) supports the delegation of user credentials across multiple remote computers. The multi-hop support functionality can use Credential Security Service Provider \(CredSSP\) for authentication. CredSSP enables an application to delegate the user’s credentials from the client computer to the target server.

CredSSP authentication is intended for environments where Kerberos delegation cannot be used. Support for CredSSP was added to allow a user to connect to a remote server and have the ability to access a second-hop machine, such as a SQL Server instance or a Domain Controller.

In some cases, a PowerShell script within SysKit Shell may need to access resources outside the remote server machine. This requires the credentials to be delegated to the target machine.

For example, when the data from SharePoint server are retrieved and a dedicated SQL Server instance needs to be accessed or when the data from Active Directory are retrieved and an underlying Domain Controller needs to be accessed.

Use the following cmdlet to enable CredSSP on the client by specifying Client in the Role parameter.

> **Please note!** The command must be executed on the **application server where SysKit Shell is installed**, and **for** the **remote server\(s\) where SysKit Shell is executing the script**.

**Enable-WSManCredSSP -Role Client –DelegateComputer \***

This policy setting allows the client to delegate explicit credentials to a remote server when server authentication is achieved. Credentials can be delegated to: **one**, **multiple** or **all** servers in a domain.

> **Please note!** If you want to tighten the security risk, instead of an asterisk, it is recommended to enter the FQDN of the remote server\(s\) where SysKit Shell is executing the script.

Use the following cmdlet to enable CredSSP on the remote server by specifying Server in Role parametar. It must be executed **on** the **remote server\(s\) where SysKit Shell is executing the script**.

**Enable-WSManCredSSP -Role Server**

This policy setting allows the remote server to act as a delegate for clients, permitting it to use delegated credentials.

The use of these two commands is shown in the image below.

![CredSSP](https://github.com/SysKitTeam/docs-shell/tree/fdfa475afe9da7e0a7441db7d0564da5a52cb19f/troubleshooting/#img/CredSSPcommands.png)

