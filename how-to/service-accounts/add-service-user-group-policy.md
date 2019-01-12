---
title: Add Service User to Local Administrators Group via Group Policy
description: >-
  This article provides guidelines on how to add the SysKit Shell service user
  to the Local Administrators security group via Group Policy on each server you
  plan to monitor.
author: Andrea Budisa
date: 25/10/2017
---

# add-service-user-group-policy

## Add Service User to Local Administrators security group through restricted groups

If you plan to monitor a lot of servers, it is much easier to configure the service user permissions via a group policy. By adding our service user to the restricted groups, you will define his privileges across your domain. You can fine-tune administrative privileges via Organizational Units.

### Create a security group in Active Directory

1. Open **Active Directory Users and Computers**, expand ‘Domain’, right-click **Users**, click **New**, and then click **Group**.
2. In the **New Object – Group** dialog box, type in **Group Name**, e.g. Local Administrators, set the Group scope to Global, and the Group type to Security. Click **OK** to proceed.
3. Right-click the newly created Group, select **Properties**, navigate to the **Members** tab, click **Add…** and enter designated users to the group, e.g. domain\administrator, domain\domain admins, domain\syskitshellservice. Add other users that also need administrative privileges, if necessary. Click **OK** to proceed.
4. Open **Group policy management** in the **Administrative tools** on your domain controller.
5. If you do not have your SysKitShell/Administrators **custom domain policy** right-click on the **Default Domain Policy** and choose **Edit**.
6. Find the policy setting **Computer Configuration** &gt; **Policies &gt; Windows settings** &gt; **Security settings** &gt; **Restricted groups**.
7. Right click on the **Restricted groups** and select **Add group**.
8. In the **Add group** dialog box, click **Browse** or type in the previously created group, e.g. domain\Local Administrators. Click **OK** to proceed.
9. Afterwards, the domain\Local Administrators Properties dialog will open.  
   If you added users or groups into the “Members of this group” box, you would advise the Restricted Groups feature to put the users and groups you selected into the ‘Local Administrators’ group. Restricted Groups would then replace the current members of the ‘Local Administrators’ group with the users and groups you filled into the box.

   As you do want to configure membership of your ‘Local Administrators’ group and assign it to the **Administrators** group on your client machines, the lower box **“This group is member of”** is the correct one.

10. Click **Add** and type in the name of the group, you want ‘Local Administrators’ to be member of. In this case, **“Administrators”**. Then click **Apply** and **OK** and close all windows.

## Set “Logon as a service user” for the SysKit Shell service user

It is important to define a Domain group policy that is going to allow the service user to “Logon as a service user.” Here is what you need to do:

1. Open **Group policy management** under Administrative tools on your domain controller.
2. If you do not have the SysKit Shell **custom domain policy**, right-click on **Default Domain Policy** and choose **Edit**.
3. Find the policy setting **Computer Configuration** &gt; **Policies** &gt; **Windows settings** &gt; **Security settings** &gt; **Local Policies** &gt; **User rights assignments** &gt; **Logon as a service** and open it with a double-click.
4. In the **Log on as a service Properties** dialog, under the Security Policy Setting tab, add the service user that you created earlier, using the Add User or Group dialog.  

   The service user will have “Logon as a service” right on each server. This step is required for SysKit Shell to run properly.

