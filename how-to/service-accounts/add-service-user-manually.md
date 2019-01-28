---
title: Add Service User to Local Administrators Group Manually
description: >-
  This article explains how to manually add the SysKit Shell service user to the
  Local Administrators security group.
author: Andrea Budisa
date: 25/10/2017
---

# Add Service User to Local Administrators Group Manually

1. Log on to the server\(s\) you plan to monitor.
2. Open **Computer Management** under Administrative tools on each server.
3. Select **Local Users and Groups** in the left navigation and then **Groups**.
4. Double-click the **Administrators** security group.
5. Add the SysKit Shell service user simply by clicking **Add** and typing the name of your SysKit Shell **service user** \(usually\).

   After adding the service user, the Administrators security group will have the members listed similarly to the following: Administrator, domain\Domain Admins.

{% hint style="warning" %}
**Please note!** You need to repeat this procedure for every server you plan to monitor with the SysKit Shell. If you plan to monitor multiple servers, we recommend adding the SysKit Shell service user via [Group Policy.](add-service-user-group-policy.md#add-service-user-to-local-administrators-security-group-through-restricted-groups)
{% endhint %}



