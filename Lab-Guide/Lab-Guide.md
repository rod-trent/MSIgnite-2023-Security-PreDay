With breaches and security incidents commonplace, many IT professionals have – both consciously and unconsciously – gained responsibilities in the security space. How do you raise your organization’s security posture when security isn’t your primary responsibility? In this interactive workshop, we’re going to show you how to optimize your organization’s security posture in a holistic manner using **Microsoft Entra**, **Microsoft Purview**, **Microsoft Defender for Cloud**, and **Microsoft Sentinel**.

**Let’s get started!**

# Microsoft Entra ID

**Microsoft Entra ID** is a cloud-based identity and access management service that enables your employees to access external resources, such as Microsoft 365, the Azure portal, and thousands of other SaaS applications.

Microsoft Entra ID helps raise your organization's security posture by providing you with a comprehensive and multicloud identity and access management solution. With Microsoft Entra ID, you can:

-   Protect your users and applications from identity attacks and risks, such as phishing, password spray, and compromised credentials. You can use features such as multifactor authentication, passwordless sign-in, conditional access, identity protection, and privileged identity management to detect and prevent unauthorized access.
-   Manage your data and resources across your hybrid and multicloud environment, including on-premises, Azure, and other cloud platforms. You can use features such as single sign-on, application proxy, entitlement management, and access reviews to grant and monitor the right access to the right resources at the right time.
-   Comply with regulatory and organizational requirements for data security and privacy, such as GDPR, HIPAA, and NIST. You can use features such as terms of use, data classification, audit logs, and reports to ensure that your data is handled in accordance with the applicable policies and standards.

Microsoft Entra ID is based on open standards and interoperable with other Decentralized Identity solutions. It is also integrated with other Microsoft security solutions, such as Microsoft 365 Defender, Defender for Cloud, and Microsoft Sentinel. By using Microsoft Entra ID, you can elevate your security posture and protect your data against risks.

## Task 1 – Create a Microsoft Entra ID Account

You are a security administrator working for a manufacturing company that produces and sells various products, such as electronics, furniture, and clothing. Your company has a hybrid and multicloud environment, consisting of multiple data centers, cloud platforms, and applications. Your company also needs to comply with various regulations and standards, such as ISO 9001, NIST 800-53, and PCI DSS, to ensure the quality and security of your products and data.

You have been tasked with implementing a secure access solution using Microsoft Entra to help your company protect and verify all types of identities and secure, manage, and govern their access to any resource across your enterprise. You will also use Entra to simplify the user experience and reduce IT friction with intelligent real-time access controls.

In this next lab, you'll access Microsoft Entra ID (previously referred to as Azure Active Directory). Additionally, you'll create a user and configure the different settings, including adding licenses.

As a subscriber to Microsoft 365, you're already using Microsoft Entra ID (previously referred to as Azure AD) to login to this lab environment. However, in this task, you’ll learn how to create a new user in Microsoft Entra ID, assign a license, and explore some of services that can be managed at the user level. Even if you’re already comfortable creating user accounts, you’ll create one here to be used for some of the additional lab tasks.

1.  Open the Microsoft Edge browser. In the address bar, enter +++**entra.microsoft.com+++** and sign in with the admin Microsoft 365 credentials provided on the Resources tab.
2.  From the left navigation pane, expand **Identity,** then **Users**, then select **All Users**. Notice that your tenant is already configured with users. The browser page to the right is the overview page of the Microsoft Entra admin center. Here you will see basic information about your Contoso tenant. If you scroll down the main window, you will also see information about alerts, my feed, feature highlights, and more.
3.  From the top of the page, select **+ New user** then from the drop-down box, select **Create new user**.
4.  You are now in the **basics** tab of creating new user page. Populate the fields as follows:
    1.  User principal name: create a user account using *Your first name and some random numbers to make it unique*

        **IMPORTANT: Remember this username. Open Notepad and copy and paste it there for reference.**

    2.  Mail nickname: leave the default, which is set to derive from user principal name.
    3.  Display name: **Your first name and a fake last name**
    4.  Password: uncheck the box that says auto-generate password and enter a temporary password that adheres to the password requirements and make note of it, as you will need it to complete the subsequent task.

        **IMPORTANT: Remember this password. Consider saving it to the same Notepad document you created just earlier for the username.**

    5.  Account enabled: Leave the checkmark to ensure the account is enabled.
    6.  At the bottom of the page, select **Next: Properties**.
5.  Here you will configure a few of the fields in the **Properties** tab.
    1.  First name: as before, *the account first name*
    2.  Last name: as before, *the account last name*
    3.  User types: Leave the default to **Member** but note that from the drop-down you have the option to select guest.

        Leave the rest of the fields as default and scroll down to the last section titled Usage location

    4.  Usage location: Choose the country/region where you are located. Note that to get to the usage location field, you will need to scroll down on the page as it is the last field on the page. **NOTE**: if you don't do this, you will not be able to assign a license in a subsequent step.
    5.  Select **Next: Assignments**.
6.  You are now on the **Assignments** tab where you add a group assignment and view the available options for adding a role.
    1.  Select **Add group**.
    2.  The window that opens shows all the available groups.
    3.  Notice the list of available groups. From the list, select **Contoso**. From the bottom of the page, select the **Select** button. It may take a few seconds, but you should see the operations group show up on the assignments page.
    4.  From the top of the page, select **Add role**. A window opens that shows all the available directory roles. View the available options, but don't add any new roles. Close this page by selecting the **X** on the top right corner of the directory roles page.
    5.  From the bottom of the page, select **Review + create**. A summary of the settings will be displayed. From the bottom of the page, select **Create**.
7.  You are returned to the user’s page. After a few seconds, the new account will be listed. You may need to select the **refresh** icon on the top of the page.
8.  From the user list, select the user you created. The **Overview** page opens.
9.  The left navigation panel shows the various options that can be configured for the user. View the available options.
10. From the left navigation panel, select **Licenses**. Notice that there are no license assignments found for this user. NOTE: Licenses can only be assigned if a usage location is configured. If you did not set the usage location, go back to that step in the previous task.
    1.  To add a license, select **+ Assignments** from the top of the main window.
    2.  Under **Select licenses**, select **Enterprise Mobility + Security E5**, **Office 365 E5** and **Windows 10/11 Enterprise E3** then select the **Save** button on the bottom of the screen. A notification on the top right corner of the screen should show that license assignments succeeded.
    3.  Select the **X** on the top right of the screen to close the License assignments window.
    4.  Select the **Refresh icon** at the top of the page to confirm the license assignments.
11. Return to the Microsoft Entra admin center by selecting **Home** from the left navigation panel or from the top-left of the screen (the breadcrumb - Home \> Users \> *your username*), above where it says your user account \| Licenses.
12. You have successfully created and configured a user in Microsoft Entra ID.
13. Sign out of all the open browser tabs. Sign out by selecting the user icon next to the email address on the top right corner of the screen then selecting **Sign out**. Close all the browser windows.

## Task 2 – Sign in with the new account

In this task, you'll sign in as your user account, for the first time.

1.  Open Microsoft Edge.
2.  In the address bar, enter +++**https://login.microsoft.com+++**.
3.  Sign in with your created user account
4.  Enter the temporary password you set in the previous task.
5.  You are now prompted to Update your password. In the Current password field, enter the temporary password from the previous task.
6.  In the New password field, enter a new password, confirm the password, then select **Sign in**. Make note of your new password (*update the Notepad document you created earlier*) as you will need it for subsequent lab exercises.
7.  You should now be successfully signed-in to Microsoft 365.
8.  Sign out by selecting the icon on the top right corner of the Microsoft 365 window that is shown as a circle with the letters that represent your initials (next to the question mark icon), then selecting **Sign out**, then close the browser.

## Task 3 - Enable passwordless phone sign-in authentication methods

Passwords are a primary attack vector. Bad actors use social engineering, phishing, and spray attacks to compromise passwords. A passwordless authentication strategy mitigates the risk of these attacks.

The Microsoft Entra admin center has a passwordless methods wizard that will help you to select the appropriate method for each of your audiences. You need administrator rights to access this wizard.

Microsoft Entra ID lets you choose which authentication methods can be used during the sign-in process. Users then register for the methods they'd like to use. The Microsoft Authenticator authentication method policy manages both the traditional push MFA method and the passwordless authentication method.

To enable the authentication method for passwordless phone sign-in, complete the following steps:

1.  Sign in to the Microsoft Entra admin center (++++https://entra.microsoft.com/++++) as at least an Authentication Policy Administrator.
2.  Browse to **Protection \> Authentication methods \> Policies**.
3.  Under Microsoft Authenticator, choose the following options:
    1.  **Enable** - Yes or No
    2.  **Target** - All users or Select users
4.  Each added group or user is enabled by default to use Microsoft Authenticator in both passwordless and push notification modes ("Any" mode). To change the mode, for each row for Authentication mode - choose Any, or Passwordless. Choosing Push prevents the use of the passwordless phone sign-in credential.
5.  To apply the new policy, click **Save**.

## Task 4 – Configuration of SSPR

**Entra Self-service Password Reset (SSPR)** is a feature that allows users to reset their passwords or unlock their accounts without contacting an administrator or help desk. It is a cloud-based service that is integrated with Microsoft Entra ID and based on open standards. Entra SSPR provides a user-friendly registration and password reset process that can be accessed from any device or location. Entra SSPR also supports password writeback, which enables users to manage their on-premises passwords through the cloud. Entra SSPR can reduce IT support costs and improve user productivity and security.

In the next lab, you, as an admin, will walk through the process of adding a user to the SSPR security group, which is already set up in your Microsoft 365 tenant. With SSPR enabled, you'll then assume the role of a user and go through the process of registering for SSPR and resetting your password. Lastly, you as the admin, will be able to view audit logs and usage data & insights for SSPR.

In this task you, as the admin, will walk through some of the available configuration settings for SSPR.

1.  Open the Microsoft Edge browser. In the address bar, enter +++**https://entra.microsoft.com+++** and sign in with the admin Microsoft 365 admin credentials provided on the Resources tab.
2.  From the left navigation pane, expand the option for **Protection**, then select **Password reset**.
3.  The properties for self-service password reset are displayed. Select the information icon next to where it says **Self services password reset enabled** to view what the description. Ensure that you’ve chosen the **Selected** option and it is highlighted. Now put your cursor over the information icon next to where it says **Select group** and note that it says, "Defines the group of users who are allowed to reset their own passwords." You must include users in the group, you can’t individually select users.
4.  Select the **No groups selected** link. This opens the **Default password reset policy** window.
5.  Select the **Contoso** group, then click **Select** button at the bottom of the screen.
6.  Once back at the **Password reset \| Properties** screen, click the **Save** button just about the **Self-service password reset enabled** message.
7.  From the left navigation panel of Password reset, select **Authentication Methods**.
8.  In the Number of methods required to rest, select **1**. Note the information box on the screen.
9.  Notice the different methods available to users. **Email** and **Mobile phone (SMS only)** should already be checked; if not, select them.
10. From the left navigation panel of Password reset, select **Registration**.
11. Ensure the setting to Require users to register when signing in is set to **Yes**. Leave the Number of days before users are asked to reconfirm their authentication information, to the default of 180. Take note of the information box on the page.
12. From the left navigation panel of Password reset, select **Notifications**.
13. Ensure the setting to Notify users on password resets is set to **Yes**. Leave the setting for Notify all admins when other admins reset their password to No.
14. Note how the Password reset navigation pane also includes options to view audit logs and Usage & insights.
15. Close the password reset window by selecting **X** on the top-right corner of the window. This returns you to the Microsoft Entra admin center.
16. Keep the Microsoft Entra window open.

## Task 5 – Managing the SSPR Security Group

Managing the SSPR Security Group in Microsoft Entra is important because it determines which users are eligible to use the self-service password reset feature. By selecting the appropriate group, you can control who can register and reset their passwords without contacting an administrator or help desk. You can also use nested groups to enable SSPR for a subset of users within a larger group. For example, you can create a test group for SSPR and add it as a member of another group that contains all your users. This way, you can test the SSPR functionality and user experience before rolling it out to everyone. You can also use the SSPR Security Group to monitor the registration and reset activity of your users and ensure compliance with your security policies.

In this task you, as the admin, will add the user you created in the previous lab exercise to the Contoso security group.

1.  Open the browser tab for the home page of the Microsoft Entra Admin center +++**entra.microsoft.com+++**. If needed, expand **Identity**.
2.  From the left navigation panel, under "Identity", expand **Groups** then select **All groups**.
3.  A list of existing groups is displayed. Select the **Contoso** security group. It will take you to the configuration option for this group.
4.  From the left navigation pane, select **Members**.
5.  From the top of the page, select **+ Add members**.
6.  In the Search box, enter **your created username**. Once the user, **your created username**, appears below the search box, select it then press **Select** from the bottom of the page. You'll be returned to the member’s page. Select **Refresh** from the top of the page. After a few seconds (you may have to hit Refresh a couple times) you should now see **your created username** listed as a member in the Contoso security group.
7.  Sign out from all the browser tabs by clicking on the user icon next to the email address on the top right corner of the screen. Then close all the browser windows.

## Task 6 – Auditing Password Reset

Viewing the audit logs and usage & insights in Entra ID is important for several reasons. Some of them are:

-   You can monitor the activity and health of your identity and access management system, such as who made what changes, when, and where.
-   You can troubleshoot issues and errors related to sign-ins, applications, groups, users, and licenses.
-   You can analyze the usage patterns and trends of your applications and authentication methods, such as which applications are most popular, which methods are most secure, and which ones need improvement.
-   You can comply with regulatory and organizational requirements for data retention and reporting.
-   You can leverage the data from the logs to optimize your identity and access strategy and improve your user experience.

In this task you, as the administrator, will briefly view the Audit logs and the Usage & Insights data associated with password reset.

1.  Open Microsoft Edge.
2.  In the address bar, enter +++**https://entra.microsoft.com+++** and sign in with the Microsoft 365 admin credentials provided on the Resources tab. If prompted for more information to login or to install Microsoft Authenticator, choose **Skip Setup**.
3.  You are in Microsoft Entra admin center. From the left navigation pane, expand the option for **Protection**, then select **Password reset**.
4.  From the left navigation pane, select **Audit logs**. Notice the information available and the available filters. Also note that you can download logs.
5.  Select **Download**. Note that you can format the download as CSV or JSON. Close the window by selecting the **X** on the top right corner of the screen.
6.  From the left navigation pane, select **Usage & insights**.
7.  Notice the information available that pertains to Registration. Note that it may take time to refresh this data, even after you do a refresh, so it may not yet reflect the registration or usage data from the previous task.
8.  From the top of the page select **Usage** to view the number of Self-service password resets and account unlocks by method. Note that it may take time to refresh this data, even after you do a refresh, so it may not yet reflect the usage data from the previous task.
9.  Close the open browser tabs.

In the next lab, you'll explore conditional access MFA, from the perspective of an admin and a user. As the admin, we will create a policy that will require a user to go through multi-factor authentication when accessing a cloud based Microsoft Azure Management application. From a user perspective, you'll see the impact of the conditional access policy, including the process to register for MFA.

## Task 7 – Reset a Password

In this task you, as the admin, will reset the password for **your created username**. This step is needed so you can initially sign in as the user in subsequent tasks.

1.  Open Microsoft Edge. In the address bar, enter +++**https://entra.microsoft.com+++**, and sign in with your admin credentials.
2.  From the left navigation pane, expand **Identity**, expand **Users**, then select **All users**.
3.  Select **your created username** from the list of users.
4.  Select **Reset password** from the top of the page.
5.  When the password reset window opens, select **Reset Password**. IMPORTANT, make a note of the new password (place this new password in the Notepad document you started earlier), as you'll need it in a subsequent task, to be able to sign in as the user.
6.  Close the password reset window by selecting the **X** at the top right corner of the page, then close out of the **your created username** window by selecting the **X** at the top right corner of the page.
7.  From the left navigation panel, select **Home** to return to the Microsoft Entra admin center.
8.  Keep this window open.

## Task 8 – Creating Conditional Access Policies

A conditional access policy in Entra ID is important because it allows you to apply the right access controls when needed to keep your organization secure. A conditional access policy is an if-then statement that evaluates various signals, such as user, device, location, application, and risk, and enforces organizational policies based on the conditions and access controls you specify. For example, you can create a policy that requires multifactor authentication for users who access sensitive applications from outside your trusted network. Conditional access policies can help you achieve the following goals:

-   Empower users to be productive wherever and whenever they need to work.
-   Protect your organization's assets from unauthorized access and potential security breaches.
-   Comply with regulatory and organizational requirements for data retention and reporting.
-   Optimize your identity and access strategy and improve your user experience.

**HOWEVER, PLEASE NOTE:** Security Defaults provide baseline protection for a tenant out of the box (require MFA for all users including Admins, block legacy auth) but its functionality is superseded by conditional access. Conditional Access policies are a way for organizations to customize access based on the needs and/or organizational policies and it may not be necessary to create Conditional Access policies for your organization. Take great care to ensure it’s absolutely necessary and even then consider using the provided templates to start with instead of creating something entirely new.

Conditional Access templates provide a convenient method to deploy new policies aligned with Microsoft recommendations. These templates are designed to provide maximum protection aligned with commonly used policies across various customer types and locations.

In this task, let’s go through and review some popular Conditional Access Policy templates.

1.  Open the browser tab to the home page of the Microsoft Entra admin center. If you previously closed the browser tab, open Microsoft Edge and in the address bar enter +++**https://entra.microsoft.com+++** and sign in with the Microsoft 365 admin credentials provided by the ALH.
2.  From the left navigation pane, expand **Protection** then select **Conditional Access**.
3.  The Conditional access overview page is displayed. Here you will see tiles showing the Policy summary and general alerts. From the left navigation panel, select **Policies**.
4.  Any existing Conditional Access Policies are listed here. Select **+ New policy from template**.
5.  Here you’ll see several template categories. 16 Conditional Access policy templates are organized into the following categories: Secure foundation, Zero Trust, Remote Work, Protect Administrator, and Emerging threats.
6.  When finished reviewing the Conditional Access policy options, close the Templates window by clicking the **X** at the top right of the windows in the Entra admin center.
7.  Details about the provided templates can be found here: ++++https://learn.microsoft.com/en-us/azure/active-directory/conditional-access/concept-conditional-access-policy-common++++

## Task 9 – The Conditional Access What If tool

The **What If** tool in Conditional Access is powerful when trying to understand why a policy was or wasn't applied to a user in a specific circumstance or if a policy would apply in a known state.

1.  The **What If** tool is located in the **Microsoft Entra admin center \> Protection \> Conditional Access \> Policies \>** **What If**. (What If is in the center of the window in the top policy menu)
2.  The What If tool requires only a User or Workload identity to get started. The following additional information is optional but helps narrow the scope for specific cases:
-   Cloud apps, actions, or authentication context
-   IP address
-   Country/Region
-   Device platform
-   Client apps
-   Device state
-   Sign-in risk
-   User risk level
-   Service principal risk (Preview)
-   Filter for devices
1.  This information can be gathered from the user, their device, or the Microsoft Entra sign-in log
2.  For details, see: ++++https://learn.microsoft.com/en-us/azure/active-directory/conditional-access/troubleshoot-conditional-access-what-if++++

# Microsoft Entra ID Governance

Microsoft Entra ID Governance is a cloud-based service that helps you manage the identity and access of your users and resources. It allows you to balance your organization's need for security and productivity with the right processes and visibility. It provides you with capabilities to ensure that the right people have the right access to the right resources at the right time. Some of the features of Microsoft Entra ID Governance are:

-   Entitlement management: You can create and manage access packages that define the resources and policies for users who need access to your applications and data.
-   Access reviews: You can review and audit the access of your users and guests to your applications, groups, and roles on a regular basis.
-   Lifecycle workflows: You can automate the provisioning and deprovisioning of user accounts and access rights based on business events and triggers.
-   Privileged identity management: You can monitor and control the access of your administrators and other privileged users to your sensitive resources and data.

Microsoft Entra ID Governance is an advanced set of identity governance capabilities available for Microsoft Entra ID P1 and P2 customers. It is based on open standards and interoperable with other Decentralized Identity solutions. Microsoft Entra ID Governance is the new name for Azure Active Directory, which reflects its expanded capabilities and vision.

In this next lab, you play the role of an IT administrator your organizations. You're asked to create an access package so employees in your organization can easily gain access to Office licenses. You want to be able to review these group members every year. You also want to allow new employees to request Office licenses, pending manager approval.

## Task 1: Configure basics for your access package

Configuring the basics of your Entra ID Governance access package is important because it allows you to define the name, description, and catalog of your access package. These are the essential information that users will see when they request or review the access package. The name and description should be clear and concise and reflect the purpose and scope of the access package. The catalog determines which resources and roles you can add to your access package, and which users can manage it. You can choose an existing catalog or create a new one, depending on your needs. By configuring the basics of your access package, you can ensure that it is well-organized and easy to use.

**Prerequisite role to accomplish this task:** Global Administrator, Identity Governance Administrator, User Administrator, Catalog Owner, or Access Package Manager

1.  Sign into the **Microsoft Entra admin center +++https://entra.microsoft.com/+++** as at least an Identity Governance Administrator.
2.  Browse to **Identity governance** \> **Entitlement management** \> **Access packages**.
3.  On the **Access packages** page Select **New access package**.
4.  On the **Basics** tab, in the **Name** box, enter **Office Licenses \#\#\#\#** *(where \#\#\#\# is a unique, random number)*. In the **Description** box, enter **Access to licenses for Office applications**.
5.  You can leave **General** in the **Catalog** list.

## Task 2: Configure the resources for your access package

Configuring the resources of your Entra ID Governance access package is important because it allows you to specify which resources and roles you want to grant access to your users. Resources can be applications, groups, or Azure resources that are in the same catalog as your access package. Roles can be application roles, group memberships, or Azure roles that define the level of access for each resource. By adding resource roles to your access package, you can ensure that your users have the appropriate and least-privilege access to the resources they need. You can also add or remove resource roles from your access package at any time, and the changes will be reflected in the existing and future assignments of the access package.

1.  Select **Next: Resource roles** to go to the **Resource roles** tab.
2.  On this tab, you select the resources and the resource role to include in the access package. In this scenario, select **Groups and Teams** and search for your group that has assigned Office licenses.
3.  Check the box beside *See all Group and Team(s) not in the ‘General’ catalog…* to show existing groups in your tenant.
4.  Select the *Contoso* group and click **Select**.
5.  Once the **Resource Roles** tab refreshes, in the **Role** dropdown list, select **Member**.

## Task 3: Configure requests for your access package

Configuring the requests for your Entra ID Governance access package is important because it allows you to define who can request the access package, how they can request it, and what happens after they request it. By configuring the requests, you can ensure that your access package is aligned with your business needs and security policies. Some of the aspects of configuring the requests are:

-   Request audience: You can specify whether the access package is for users in your directory, users in connected organizations, or any external user. You can also limit the request audience to specific groups or domains.
-   Request mode: You can choose whether users can request the access package directly, or if they need to be nominated by an administrator or another user.
-   Request settings: You can customize the request form that users see when they request the access package. You can add questions, instructions, terms of use, and verified ID requirements to the form.
-   Approval settings: You can define who needs to approve the access requests, and how many approvals are required. You can choose from predefined approvers, such as resource owners or group owners, or select custom approvers, such as managers or specific users.
-   Lifecycle settings: You can set how long the access package assignments last, and whether they need to be renewed or reviewed periodically. You can also enable expiration notifications and reminders for users and approvers.

By configuring these settings, you can manage the requests for your access package effectively and efficiently.

1.  Select **Next: Requests** to go to the **Requests** tab.
2.  On this tab, you create a request policy. A *policy* defines the rules for access to an access package. You create a policy that allows employees in the resource directory to request the access package.
3.  In the **Users who can request access** section, select **For users in your directory** and then select **All members (excluding guests)**. These settings make it so that only members of your directory can request Office licenses.
4.  Ensure that **Require approval** is set to **Yes**.
5.  Leave **Require requestor justification** set to **Yes**.
6.  Leave **How many stages** set to **1**.
7.  Under **Approver**, select **Manager as approver**. This option allows the requestor's manager to approve the request. You can select a different person to be the fallback approver if the system can't find the manager.
8.  Leave **Decision must be made in how many days?** set to **14**.
9.  Leave **Require approver justification** set to **Yes**.
10. Under **Enable new requests and assignments**, select **Yes** to enable employees to request the access package as soon as it's created.

## Task 4: Configure requestor information for your access package

1.  Select **Next** to go to the **Requestor information** tab.
2.  On this tab, you can ask questions to collect more information from the requestor. The questions are shown on the request form and can be either required or optional. In this scenario, you haven't been asked to include requestor information for the access package, so you can leave these boxes empty.

## Task 5: Configure the lifecycle for your access package

1.  Select **Next: Lifecycle** to go to the **Lifecycle** tab.
2.  In the **Expiration** section, for **Access package assignments expire**, select **Number of days**.
3.  In **Assignments expire after**, enter **365**. This box specifies when members who have access to the access package need to renew their access.
4.  You can also configure access reviews, which allow periodic checks of whether the employee still needs access to the access package. A review can be a self-review performed by the employee. Or you can set the employee's manager or another person as the reviewer.
5.  In this scenario, you want all employees to review whether they still need a license for Office each year.
    1.  Under **Require access reviews**, select **Yes**.
    2.  You can leave **Starting on** set to the current date. This date is when the access review starts. After you create an access review, you can't update its start date.
    3.  Under **Review frequency**, select **Annually**, because the review occurs once per year. The **Review frequency** box is where you determine how often the access review runs.
    4.  Specify a **Duration (in days)**. The duration box is where you indicate how many days each occurrence of the access review series runs.
    5.  Under **Reviewers**, select **Manager**.

## Task 6: Review and create your access package

1.  Select **Next: Review + Create** to go to the **Review + Create** tab.
2.  On this tab, you can review the configuration for your access package before you create it. If there are any problems, you can use the tabs to go to a specific point in the process to make edits.
3.  When you're happy with your configuration, select **Create**. After a moment, you should see a notification stating that the access package is created.
4.  After the access package is created, you'll see the **Overview** page for the package.

## Task 7: Clean up resources

In this step, you can delete the Office Licenses access package to prepare the lab environment of other tasks.

**Prerequisite role:** Global Administrator, Identity Governance Administrator, or Access Package Manager

1.  Sign into the Microsoft Entra admin center ++https://entra.microsoft.com/ ++ as at least an Identity Governance Administrator.
2.  Browse to **Identity governance** \> **Entitlement management** \> **Access package**.
3.  Open the **Office Licenses** access package.
4.  Select **Resource Roles**.
5.  Select the group you added to the access package. On the details pane, select **Remove resource role**. In the message box that appears, select **Yes**.
6.  Open the list of access packages.
7.  For **Office Licenses**, select the ellipsis button (...) and then select **Delete**. In the message box that appears, select **Yes**.

# Microsoft Entra Workload ID

Access reviews for Microsoft Entra Workload ID are important because they allow you to review and audit the access of your service principals to your enterprise applications and resources. Service principals are identity objects that represent applications or automated processes that need to access your resources. By reviewing the access of your service principals, you can ensure that they have the appropriate and least-privilege permissions to perform their tasks. You can also reduce the risk of unauthorized or malicious access by removing or revoking stale or unused service principal assignments. Access reviews for Microsoft Entra Workload ID require a Microsoft Entra Workload ID Premium plan in addition to Microsoft Entra ID P2 or Microsoft Entra ID Governance licenses.

You are the administrator of a company that uses Microsoft Entra Workload ID to manage and secure identities for digital workloads, such as apps and services. You want to create access review accounts that have access to a critical Azure resource group. You want to ensure that only the accounts that need access to this resource group have it and remove any unnecessary or risky access.

### Task 1: Create access reviews

1.  Sign into the **Microsoft Entra admin center +++https://entra.microsoft.com/+++** .
2.  Browse to **Identity governance** \> **Privileged Identity Management**.
3.  For **Microsoft Entra roles**, select **Azure AD Roles/Microsoft Entra roles**.
4.  Select **Roles** again under **Manage** to review available roles.
5.  Under Manage, select **Access reviews**, and then select **New** to create a new access review.
6.  Name the access review. Optionally, give the review a description. The name and description are shown to the reviewers.
7.  Set the **Start date**. By default, an access review occurs once, starts the same time it's created, and it ends in one month. You can change the start and end dates to have an access review start in the future and last however many days you want.
8.  To make the access review recurring, change the **Frequency** setting from **One time** to **Weekly**, **Monthly**, **Quarterly**, **Annually**, or **Semi-annually**. Use the **Duration** slider or text box to define how many days each review of the recurring series will be open for input from reviewers. For example, the maximum duration that you can set for a monthly review is 27 days, to avoid overlapping reviews.
9.  Use the **End** setting to specify how to end the recurring access review series. The series can end in three ways: it runs continuously to start reviews indefinitely, until a specific date, or after a defined number of occurrences has been completed. You, or another administrator who can manage reviews, can stop the series after creation by changing the date in **Settings**, so that it ends on that date.
10. In the **Users Scope** section, select the scope of the review. For **Microsoft Entra roles**, the first scope option is Users and Groups. Directly assigned users and role-assignable groups will be included in this selection. For **Azure resource roles**, the first scope will be Users. Groups assigned to Azure resource roles are expanded to display transitive user assignments in the review with this selection. You may also select **Service Principals** to review the machine accounts with direct access to either the Azure resource or Microsoft Entra role.
11. Or, you can create access reviews only for inactive users (preview). In the *Users scope* section, set the **Inactive users (on tenant level) only** to **true**. If the toggle is set to *true*, the scope of the review will focus on inactive users only. Then, specify **Days inactive** with a number of days inactive up to 730 days (two years). Users inactive for the specified number of days will be the only users in the review.
12. Under **Review role membership**, select the privileged Azure resource or Microsoft Entra roles to review.
13. **Note**
14. Selecting more than one role will create multiple access reviews. For example, selecting five roles will create five separate access reviews.
15. In **assignment type**, scope the review by how the principal was assigned to the role. Choose **eligible assignments only** to review eligible assignments (regardless of activation status when the review is created) or **active assignments only** to review active assignments. Choose **all active and eligible assignments** to review all assignments regardless of type.
16. In the **Reviewers** section, select one or more people to review all the users. Or you can select to have the members review their own access.
    1.  **Selected users** - Use this option to designate a specific user to complete the review. This option is available regardless of the scope of the review, and the selected reviewers can review users, groups and service principals.
    2.  **Members (self)** - Use this option to have the users review their own role assignments. This option is only available if the review is scoped to **Users and Groups** or **Users**. For **Microsoft Entra roles**, role-assignable groups will not be a part of the review when this option is selected.
    3.  **Manager** – Use this option to have the user’s manager review their role assignment. This option is only available if the review is scoped to **Users and Groups** or **Users**. Upon selecting Manager, you will also have the option to specify a fallback reviewer. Fallback reviewers are asked to review a user when the user has no manager specified in the directory. For **Microsoft Entra roles**, role-assignable groups will be reviewed by the fallback reviewer if one is selected.

# Microsoft Purview

Microsoft Purview is a family of data governance, risk, and compliance solutions that can help your organization govern, protect, and manage your entire data estate. Microsoft Purview helps you raise your organization's security posture by enabling you to:

-   Gain visibility into data assets across your organization, including on-premises, multi-cloud, and software-as-a-service (SaaS) sources.
-   Identify and classify sensitive data across your data estate, and apply appropriate protection policies to prevent unauthorized access or leakage.
-   Monitor and audit the activity and health of your identity and access management system, and detect and respond to data risks and threats.
-   Comply with regulatory and organizational requirements for data retention and reporting, and leverage data insights to optimize your data strategy.

In this lab, you are a data engineer working for a healthcare organization that provides various services to patients, such as diagnosis, treatment, medication, and surgery. Your organization has a large and complex data estate, consisting of multiple data sources, such as electronic health records, medical images, lab results, billing systems, and external data providers. Your organization also needs to comply with various regulations and standards, such as HIPAA, GDPR, and ISO 27001, to ensure the privacy and security of your data.

You have been tasked with implementing a data governance solution using Microsoft Purview to help your organization discover, catalog, and understand all your data across your enterprise. You will also use Purview to manage and govern your data with policies, roles, and access controls.

In this lab you'll configure and prepare your environment for administration tasks. By following the steps provided, you'll ensure that essential features and settings are enabled in advance, allowing for an easier learning experience in upcoming lab activities. This preparation will include activating necessary features, setting up administrative permissions, and ensuring the proper configuration of key elements.

## Task 1 – Create user accounts and passwords for lab exercises

Getting started: In this task, you'll set passwords for the user accounts that will be needed for the other tasks in this lab.

1.  In **Microsoft Edge**, navigate to +++**https://admin.microsoft.com+++** and log into the portal as the M365 Administrator ID provided by your lab hosting provider.
2.  On the left navigation pane, expand **Users** then select **Active users**.
3.  On the **Active users** page, Create a new user account. Give the new user account a unique name.
4.  Once the user is created, select the **Reset password** key and the **Reset password** flyout page should appear on the right to reset the user’s password.
5.  Ensure none of the checkboxes are selected on the **Reset password** flyout page.
6.  In the **Password** field, enter a password for the user account you can remember.
7.  **IMPORTANT: Remember this username and password. Open Notepad and copy and paste it there for reference.**
8.  Select the **Reset password** button to reset the user’s password.
9.  On the **Password has been reset** page, select the **Close** button to go back to the **Active users** page.
10. Repeat steps 4-8 to create two additional user accounts. Also place the information for these accounts into the Notepad document for later reference.

## Task 2 - Enabling Auditing in the Microsoft Purview portal

The importance of enabling audit in the Microsoft Purview portal is that it allows you to record and retain the user and admin activity in your data estate. By enabling audit, you can:

-   Gain visibility into the data assets across your organization, including on-premises, multi-cloud, and software-as-a-service (SaaS) sources.
-   Identify and classify sensitive data across your data estate and apply appropriate protection policies to prevent unauthorized access or leakage.
-   Monitor and audit the activity and health of your identity and access management system and detect and respond to data risks and threats.
-   Comply with regulatory and organizational requirements for data retention and reporting, and leverage data insights to optimize your data strategy.

In this task, you'll enable Audit in the Microsoft Purview compliance portal. This tracking feature ensures visibility and accountability by monitoring portal activities.

1.  In **Microsoft Edge**, navigate to +++**https://compliance.microsoft.com+++**.
2.  In the left navigation pane select **Audit**.
3.  On the **Audit** page. select **Start recording user and admin activity** to activate audit logging.

## Task 3 – Assign Compliance Roles

Assigning Compliance Roles in Microsoft Purview is important because it allows you to control who can perform various compliance tasks and access different features in the Microsoft Purview compliance portal. By assigning Compliance Roles, you can:

-   Ensure that your users have the appropriate and least privilege permissions to do their jobs across compliance solutions, such as device management, data loss prevention, eDiscovery, insider risk management, retention, and more.
-   Manage the permissions for users who perform compliance tasks in Microsoft 365 services, such as Exchange Online, SharePoint Online, OneDrive for Business, Teams, and Yammer.
-   Comply with regulatory and organizational requirements for data security and privacy, such as GDPR, HIPAA, and NIST.
-   Monitor and audit the activity and health of your identity and access management system and detect and respond to data risks and threats.

As the recently hired Compliance Administrator for Contoso Ltd. in the role of Joni Sherman, your responsibility is to configure your organization's new Microsoft 365 tenant to meet its compliance requirements. Contoso Ltd. is a company headquartered in the United States with new subsidiaries in the European Union, and it is essential for your organization to ensure that the new Microsoft 365 tenant complies with legal requirements in different countries and regulatory standards in your industry sector.

In this task, you will follow the principal of least privilege and use the default Global Administrator to assign the Compliance Admin role to your created user account, which is required to perform the operations described in this lab.

1.  Open **Microsoft Edge**, select the address bar, navigate to +++**https://admin.microsoft.com+++** and log into the Microsoft 365 admin center as **M365 Administrator ID** provided by your lab hosting provider.
2.  On the **Stay signed in?** dialog box, select the **Don’t show this again** checkbox and then select **No**.
3.  Close the password save dialog from the bottom by selecting **Never**, to not save the default global admins credentials in your browser.
4.  If a welcome screen is displayed, close it. If the Office 365 apps notification appears, also close it.
5.  If a welcome window is displayed, select Get started and close it.
6.  In the left navigation pane, expand **Users** then select **Active users**.
7.  In the **Active users** list select **Joni Sherman**. This will open a flyout page to the right with Joni's user settings.
8.  In User’s user setting page, select **Reset password**. On the **Reset password** page deselect **Automatically create a password** and **Require this user to change their password when they first sign in**. There should be no options enabled on this page.
9.  In the **Password** field, enter a password for Joni's account that you'll remember then select the **Reset password** button.
10. Once the user’s password has been reset, you'll see a message confirming **Password has been reset**. Select the back arrow on the upper left of this page to go back to Joni's user settings page.
11. On the User’s user settings page, below the **Account** tab, scroll to **Roles** then select **Manage roles**.
12. On the **Manage admin roles** flyout page, select **Admin center access** then scroll down to select **Show all by category**. Under the category view in the **Security & Compliance** category select **Compliance Administrator** .
13. Select **Save changes** to apply the role. When the **Admin roles updated** message is displayed on the upper part of the page, select the arrow pointing to the left to return to Joni's user settings.
14. Close the flyout page displaying the user’s account with the **X** in the upper right to go back to the **Active users** list.
15. Before switching to the user account, use the Global Admin privileges of M365 Administrator for activating the audit logging by navigating to +++https://compliance.microsoft.com/auditlogsearch+++.
16. On the **Audit** page. select **Start recording user and admin activity** to activate audit logging.
17. Select the circle with **MA** in the upper right and select **Sign out**.
18. Close the **Microsoft Edge** browser window.

You have successfully assigned the User account the Compliance Administrator role, which is required to perform the different exercises of this lab. Continue with the next task.

## Task 4 – Explore the Microsoft Purview portal

In this task, you will sign out of the global admin account and sign-in again as the user account. Now that the user is assigned the Compliance admin role, the account will be sufficient for most of this lab's exercises.

1.  In **Microsoft Edge**, navigate to +++**https://compliance.microsoft.com+++**.
2.  When the **Pick an account** window is displayed, select **Use another account**.
3.  When the **Sign in** window is displayed, sign in as the user account you created.
4.  If the **Improve your compliance posture** message window opens, read the text and select **Next** twice and then select **Done**.
5.  The page **Welcome to the Microsoft Purview compliance portal** is displayed. Investigate the dashboard tiles and the left-side navigation pane.
6.  Get yourself familiar with the different settings. When you are done, leave the browser window open.

## Task 5 – Create Sensitivity Labels

Sensitivity labels are tags that you can apply on assets to classify and protect your data. They help you to state how sensitive certain data is in your organization and enforce appropriate policies based on the labels. For example, you can apply a "Confidential" label to a document or email, and that label encrypts the content and applies a "Confidential" watermark¹. Sensitivity labels can also be applied to containers, such as Teams, Microsoft 365 Groups, and SharePoint sites, to control their settings and access. Sensitivity labels can be created and configured in the Microsoft Purview compliance portal, and they can be automatically or manually applied to your data in the Microsoft Purview Data Map. Sensitivity labels are based on open standards and interoperable with other Decentralized Identity solutions.

In this lab you will assume the role of the user account you have created. Your organization is based in Rednitzhembach, Germany and is currently implementing a sensitivity plan to ensure that all employee documents in the HR department have been marked with a sensitivity label as part of your organizations information protection policies.

In this task, your HR department has requested a sensitivity label to apply to HR employee documents. You will create a sensitivity label for Internal documents and a sublabel for the HR department.

1.  In **Microsoft Edge**, navigate to +++**https://compliance.microsoft.com+++** and log into the Microsoft Purview portal as your created user account.
2.  In the Microsoft Purview portal, on the left navigation pane, expand **Information protection** then select **Labels**.
3.  On the **Labels** page select **+ Create a label**.
4.  The **New sensitivity label** wizard will start. On the **Name and create a tooltip for your label** page for the **Name**, **Description for admins** and **Description for users**, enter the following information:
    1.  **Name**: Internal
    2.  **Display name**: Internal
    3.  **Description for users**: Internal sensitivity label.
    4.  **Description for admins**: Internal sensitivity label for Contoso.
5.  Select **Next**.
6.  On the **Define the scope for this label** page, select **Items** and select **Files** and **Emails**. If any other options on this page are selected, deselect those options.
7.  Select **Next**.
8.  On the **Choose protection settings for labeled items** page, select **Next**.
9.  On the **Auto-labeling for files and emails** page, select **Next**.
10. On the **Define protection settings for groups and sites** page, select **Next**.
11. On the **Auto-labeling for schematized data assets (preview)** page, select **Next**.
12. On the **Review your settings and finish** page, select **Create label**.
13. Once the label has been created **Your sensitivity label was created** page will be displayed.
14. Select **Don't create a policy yet** and then select **Done**.
15. On the Information protection page, highlight (without selecting) the newly created **Internal** label and select the vertical **...**
16. Select the **+ Create sublabel** from the drop-down menu.
17. The **New sensitivity label** wizard will start. On the **Name and create a tooltip for your label** page for the **Name**, **Display Name**, **Description for admins** and **Description for users**, enter the following information:
    1.  **Name**: Employee data (HR)
    2.  **Display name**: Employee data (HR)
    3.  **Description for users**: This HR label is the default label for all specified documents in the HR Department.
    4.  **Description for admins**: This label is created in consultation with Ms. Jones (Head of HR department). Contact her when you want to change settings of the label.
18. Select **Next**.
19. On the **Define the scope for this label** page, select the option **Items** and select **Files** and **Emails**.
20. Select **Next**.
21. On the **Choose protection settings for labeled items** page, select the **Apply or remove encryption** option.
22. Select **Next**.
23. On the **Encryption** page select **Configure encryption settings**.
24. Enter the following information into the encryption settings:
    1.  **Assign permissions now or let users decide?**: Assign permissions now
    2.  **User access to content expires**: Never
    3.  **Allow offline access**: Only for a number of days
    4.  **Users have offline access to the content for this many days**: 15
25. Select the **Assign permissions** link,
26. On the Assign permissions side menu, select the **+ Add any authenticated users**.
27. Select **Save**.
28. On the **Encryption** page, select **Next**.
29. On the **Auto-labeling for files and emails** page, select **Next**.
30. On the **Define protection settings for groups and sites** page, select **Next**.
31. On the **Auto-labeling for schematized data assets (preview)** page, select **Next**.
32. On the **Review your settings and finish** page, select **Create label**.
33. The label will be created and when complete a message will display **Your sensitivity label was created**.
34. Select **Don't create a policy yet** and then select **Done**.

You have successfully created a sensitivity label for your organization’s internal policies and a sensitivity sublabel for the Human Resources (HR) department.

## Task 6 – Publish Sensitivity Labels

You will now publish the Internal and HR sensitivity label so that the published sensitivity labels will be available for the HR users to apply to their HR documents.

1.  In **Microsoft Edge**, the Microsoft Purview portal tab should still be open. If so, select it and proceed to the next step. If you closed it, then in a new tab, navigate to +++**https://compliance.microsoft.com+++**.
2.  In the Microsoft Purview portal, on the left navigation pane, expand **Information protection** then select **Labels**.
3.  On the Labels page select **Publish label**.
4.  The publish sensitivity labels wizard will start.
5.  On the **Choose sensitivity labels to publish** page, select the **Choose sensitivity labels to publish** link.
6.  The **Sensitivity labels to publish** pane will appear on the right.
7.  Select the **Internal** and **Internal/Employee Data (HR)** checkboxes.
8.  Select **Add**.
9.  On the **Choose sensitivity labels to publish** page, select **Next**.
10. On the **Assign admin units (preview)** page, select **Next**
11. On the **Publish to users and groups** page, select **Next**.
12. On the **Policy settings** page, select **Next**.
13. On the **Default settings for documents** select **Next**.
14. On the **Default settings for emails** select **Next**.
15. On the **Default settings for meetings and calendar events** select **Next**.
16. On the **Default settings for Power BI Content** select **Next**.
17. On the **Name your policy** page, enter the following information:
    1.  **Name**: Internal HR employee data
    2.  **Enter a description for your sensitivity label policy**: This HR label is to be applied to internal HR employee data.
18. Select **Next**.
19. On the **Review and finish** page, select **Submit**.
20. On the **New policy created**, select **Done** to finish publishing your label policy.

You have successfully published the Internal and HR sensitivity labels. Note that it can take up to 24 hours for changes to replicate to all users and services.

## Task 7 – Configure Auto Labeling

Auto labeling is important in Microsoft Purview because it helps you to classify and protect your data assets automatically, without relying on manual intervention or user training. Auto labeling can help you to:

-   Apply consistent and accurate sensitivity labels to your data based on the content and context of the data.
-   Enforce data protection policies and actions based on the sensitivity labels, such as encryption, access control, retention, and deletion.
-   Track and audit the usage and activity of your sensitive data across different sources and locations.
-   Comply with data privacy and security regulations and standards, such as GDPR, HIPAA, PCI DSS, etc.

You can use auto labeling in Microsoft Purview to label files and database columns in the data map, as well as files and emails in SharePoint, OneDrive, and Exchange. You can create auto labeling rules for each sensitivity label, defining which classification or sensitive information type constitutes a label.

In this task, you will create a Sensitivity Label that will auto label documents and emails found to contain information related to the European General Data Protection Regulation (GPDR).

1.  In **Microsoft Edge**, navigate to +++**https://compliance.microsoft.com+++** and log into the Microsoft Purview portal as **you created user account**.
2.  In the Microsoft Purview portal, on the left navigation pane, expand **Information protection** and then select **Labels**.
3.  On the Labels page, highlight (without selecting) the existing **Internal** label, and select the three dots.
4.  Select the **+ Create sublabel** menu item.
5.  The **New sensitivity label** wizard will start. On the **Name and create a tooltip for your label** page, enter the following information:
    1.  **Name**: GDPR Germany
    2.  **Display name**: GDPR Germany
    3.  **Description for users**: This document or email contains data related to the European General Data Protection Regulation (GPDR) for the region Germany.
    4.  **Description for admins**: This label is auto applied to German GDPR documents.
6.  Select **Next**.
7.  On the **Define the scope for this label** page, select the option **Items** and select **Files** and **Emails**.
8.  Select **Next**.
9.  On the **Choose protection settings for labeled items** page, select **Next**.
10. On the **Auto-labeling for files and emails** page, set the **Auto-labeling for files and emails** to enabled.
11. In the **Detect content that matches these conditions** section, select **+Add condition** then select **Content contains**.
12. In **Content contains** section select the **Add** text then select **Sensitive info types**.
13. A **Sensitive info types** panel will be displayed on the right.
14. In the **Search for sensitive info types** search panel, enter the following information:
15. German
16. Press the enter button, the results will display sensitivity info types related to Germany.
17. Press the **Select all** check box.
18. Select **Add**.
19. Select **Next**.
20. On the **Define protection settings for groups and sites** page, select **Next**.
21. On the **Auto-labeling for schematized data assets (preview)** page, select **Next**.
22. On the **Review your settings and finish** page, select **Create label**.
23. The label will be created and when complete a message will display: **Your sensitivity label was created**.
24. Select **Done**.
25. Once the label has been created the **Your sensitivity label was created** page will be displayed.
26. Select **Don't create a policy yet** and then select **Done**.
27. On the **Labels** page, select **Publish label**.
28. The Publish sensitivity labels wizard will start.
29. On the **Choose sensitivity labels to publish** page, select the **Choose sensitivity labels to publish** link.
30. A side bar called **Sensitivity labels to publish** will appear on the right.
31. Select the **Internal** and **Internal/GDPR Germany** checkbox.
32. Select **Add**.
33. On the **Choose sensitivity labels to publish** page, select **Next**.
34. On the **Assign admin units (preview)** page, select **Next**.
35. On the **Publish to users and groups** page, select **Next**.
36. On the **Policy settings** page, select **Next**.
37. On the **Default settings for documents​** page, select **Next**.
38. On the **Default settings for emails** page, select **Next**.
39. On the **Default settings for meetings and calendar events** page, select **Next**.
40. On the **Default settings for Power BI content** page, select **Next**.
41. On the **Name your policy** page, enter the following information:
    1.  **Name**: GDPR Germany policy
    2.  **Enter a description for your sensitivity label policy**: This auto apply sensitivity labels policy is for the GDPR region of Germany.
42. Select **Next**.
43. On the **Review and finish** page, select **Submit**.
44. The policy will be created and when complete a message will display, **New policy created**.
45. Select **Done**.

You have successfully created and published an auto apply sensitivity label for GDPR documents in the region Germany.

Be aware that it can take up to 24 hours for auto applied sensitivity labels to be applied, this duration will be longer when applied to more than 25,000 documents (that is, the daily limit).

You are **your created user account**, the newly hired Compliance Administrator for Contoso Ltd. tasked to configure the company's Microsoft 365 tenant for data loss prevention. Contoso Ltd. is a company that offers driving instruction in the United States, and you need to make sure that sensitive customer information does not leave the organization.

## Task 8 – Create a DLP policy

A **Data Loss Prevention (DLP) policy** in Microsoft Purview is a set of rules that define how to identify, monitor, and protect sensitive data across different platforms and devices. DLP is a discipline that helps prevent the accidental or intentional sharing of sensitive information that could cause harm to your organization or customers. A DLP policy can help you to:

-   Detect sensitive data based on the content and context of the data, using built-in or custom sensitive information types, classification labels, or trainable classifiers.
-   Apply actions to protect sensitive data, such as blocking access, encrypting, notifying users, generating alerts, or creating reports.
-   Enforce data protection policies consistently across Microsoft 365 services such as Teams, Exchange, SharePoint, and OneDrive accounts, as well as Windows 10 and Windows 11 devices.
-   Comply with data privacy and security regulations and standards, such as GDPR, HIPAA, PCI DSS, etc.

You can create and manage DLP policies in the Microsoft Purview compliance portal, using a user-friendly interface that guides you through the policy creation process. You can also use PowerShell cmdlets or Graph APIs to create and manage DLP policies programmatically.

In this exercise, you will create a Data Loss Prevention policy in the Microsoft Purview portal to protect sensitive data from being shared by users. The DLP Policy that you create will inform your users if they want to share content that contains Credit Card information and allow them to provide a justification for sending this information. The policy will be implemented because you do not want the block action to affect your users yet.

1.  In **Microsoft Edge**, navigate to +++**https://compliance.microsoft.com+++** and log into the Microsoft Purview portal as your user account.
2.  If the **Stay signed in?** dialog box appears, select the **Don’t show this again** checkbox and then select **No**.
3.  In the **Microsoft Purview** portal, in the left navigation pane, expand **Data loss prevention** then select **Policies**.
4.  On the **Policies** page select **+Create policy** to start the wizard for creating a new data loss prevention policy.
5.  On the **Start with a template or create a custom policy** page, scroll down and select **Custom** under **Categories** and **Custom policy** under **Templates**. By default, both options should already be selected, select **Next**.
6.  On the **Name your DLP policy** page enter:
    1.  **Name**: Credit Card DLP Policy
    2.  **Description**: Protect credit card numbers from being shared
7.  Select **Next**.
8.  On the **Assign admin units (preview)** page select **Next**.
9.  On the **Choose locations to apply the policy** page, enable the **Teams chat and channel messages** option only and select **Next**.
10. On the **Define policy settings** page, select **Create or customize advanced DLP rules** and select **Next**.
11. On the **Customize advanced DLP rules** page, select **+ Create rule**.
12. On the **Create rule** flyout page, type *Credit card information* in the **Name** field.
13. Under **Conditions**, select **+ Add Condition** and then select **Content contains** from the dropdown menu.
14. In the new **Content contains** area, select **Add** and select **Sensitive info types** from the dropdown menu.
15. On the **Sensitive info types** page, select **Credit Card Number** and select **Add**.
16. On the **Create rule** page, select **+ Add condition** and select **Content is shared from Microsoft 365** from the dropdown menu.
17. In the new **Content is shared from Microsoft 365** section, select the **only with people inside my organization** option.
18. On the **Create rule** page, select **+ Add an action**. Under **Use actions to protect content when the conditions are met.** expand **Restrict access or encrypt the content in Microsoft 365 locations** and select **Block everyone.**
19. On the **Create rule** page, in the **User notifications** section, select the switch to **On** to enable user notifications.
20. Select the check box to enable **Notify users in Office 365 service with a policy tip**.
21. Under **User overrides** select the checkbox to **Allow overrides from M365 services. Allows users in Exchange, SharePoint, OneDrive and Teams to override policy restrictions.**
22. Check the checkbox to **Require a business justification to override**.
23. In the **Incident reports** section, in the **Use this severity level in admin alerts and reports** dropdown, select **Low**.
24. On the **Create rule** page select **Save** then select **Next**.
25. On the **Policy** page select **Test it out first** and select **Show policy tips while in test mode**.
26. On the **Review your policy and create it** page review your settings then select **Submit**
27. On the **New policy created** page select **Done**.

You have now created a DLP policy that scans Credit Card numbers in Microsoft Teams chats and channels and allows users to provide a business justification to override the policy.

## Task 9 - Modify a DLP policy

In this task, you will Modify the existing DLP policy you created in the previous step to also scan e-mails for Credit Card information and inform users if they want to share this content in an e-mail.

1.  In **Microsoft Edge**, the Microsoft Purview portal tab should still be open. If so, select it and proceed to the next step. If you closed it, then in a new tab, navigate to +++**https://compliance.microsoft.com+++**.
2.  In the **Microsoft Purview** portal, in the left navigation pane, expand **Data loss prevention** then select **Policies**.
3.  On the **Policies** page select the checkbox next to the recently created **Credit Card DLP Policy** and then select **Edit policy** (pencil icon) to open the policy wizard.
4.  On the **Name your DLP policy** page, select **Next**.
5.  On the **Assign admin units (preview)** page select **Next**.
6.  On the **Choose locations to apply the policy** page, enable the **Exchange email** option and then select **Next** until you reach the **Review your policy and create it** page.
7.  Select **Submit** to apply the change you made to the policy.
8.  Once the policy is updated select **Done**.

You have now modified an existing DLP policy and changed the locations it scans for content.

## Task 10 - Enable file monitoring in Microsoft 365 Defender

You want to use file policies in Microsoft 365 Defender to protect files in your OneDrive and SharePoint Online locations. Before you can create a file policy, you need to enable file monitoring so Microsoft 365 Defender can scan files in your organization.

It is important to enable file monitoring in Microsoft Defender because it helps you to:

-   Detect and protect sensitive data across different platforms and devices, using sensitivity labels, sensitive information types, or trainable classifiers.
-   Apply data protection policies and actions based on the sensitivity labels, such as encryption, access control, retention, and deletion.
-   Track and audit the usage and activity of your sensitive data across different sources and locations.
-   Comply with data privacy and security regulations and standards, such as GDPR, HIPAA, PCI DSS, etc.

To do this:

1.  In **Microsoft Edge**, the Microsoft Purview portal tab should still be open. Select the **Profile picture** of your created user account in the top right and select **Sign out**, then close the browser.
2.  Open **Microsoft Edge** and navigate to +++**https://security.microsoft.com+++** and log into the Microsoft 365 Defender portal as **M365 Administrator** ID provided by your lab hosting provider.
3.  On the left navigation pane, scroll down then select **Settings**.
4.  On the **Settings** page select **Cloud Apps**.
5.  In the left pane within the **Cloud apps** window, scroll down to the **Information Protection** section, then select **Files**.
6.  Select the **Enable file monitoring** checkbox then select **Save** if it is not already marked.

You successfully enabled file monitoring in Microsoft 365 Defender and can now scan files for sensitive content using file policies.

## Task 11 - Create a file policy for Microsoft 365 Defender

With File Monitoring now enabled, you want to create a file policy in Microsoft 365 Defender to scan files in OneDrive and SharePoint Online and automatically quarantine files containing credit card information if they are shared.

1.  In **Microsoft Edge**, the Microsoft Defender for Cloud Apps portal tab should still be open. Select the **Profile picture** of the M365 Admin in the top right and select **Sign out** next to the cogwheel, then close the browser.
2.  Open **Microsoft Edge** and navigate to +++**https://security.microsoft.com+++** and log into the Microsoft 365 Defender portal as your created user account.
3.  In the **Microsoft 365 Defender** portal, in the left navigation, scroll down to the **Cloud apps** section, then select **Files**.
4.  On the **Files** page select **+ New policy from search**.
5.  On the **Create file policy** page, leave the **Policy template** selection as **No template**.
6.  Enter this information on the **Create file policy** page
    1.  **Policy name**: Credit Card Information for files
    2.  **Description**: Protect credit card numbers from being shared in files
7.  Keep the **Policy Severity** on **Low** (one lighted icon) and make sure the **Category** is set to **DLP**. For a file policy, this should be the default.
8.  In the **Files matching all of the following** area, expand the dropdown menu **Public (Internet), External, Public** and add **Internal**.
9.  In the **Inspection Method** dropdown menu, select **Data Classification Service**.
10. In the **Choose inspection type...** dropdown menu, select **Sensitive information type...**.
11. On the **Select a sensitive information type** dialog, select **Credit Card Number**, then select **Done** in the upper right corner.
12. Under **Alerts**, check the **Create an alert for each matching file** checkbox and review your options. Keep the settings as the default by selecting **Save as default settings**.
13. In the **Governance actions** section, expand **Microsoft OneDrive for Business** and select **Put in user quarantine**.
14. In the **Governance actions** section, expand **Microsoft SharePoint Online** and select the checkbox for **Put in user quarantine**.
15. Select **Create** at the bottom of the page.

You have now created a file policy that will continuously scan files saved in OneDrive and SharePoint for credit card information and quarantine them if they are shared inside your organization.

In this exercise, you will assume the role of Joni Sherman, a System Administrator for Contoso Ltd. Your organization is based in Texas and wants to implement retention policies to adhere to state laws, which stipulates that records may be deleted after three years without constituting an offense.

In order to adhere to this law your organization has created a retention plan to retain all items in the organization for three years.

## Task 12 – Create company-wide Retention Policy

Creating a company-wide retention policy in Purview is important because it can help you to:

-   Manage the data lifecycle for your organization by deciding proactively whether to retain content, delete content, or retain and then delete the content.
-   Apply consistent and accurate retention settings across different data sources and locations, such as Microsoft 365, SharePoint, OneDrive, Teams, Exchange, etc.
-   Reduce your risk in the event of litigation or a security breach by permanently deleting old content that you're no longer required to keep.
-   Comply with data privacy and security regulations and standards, such as GDPR, HIPAA, PCI DSS, etc.

In this exercise you will create a company-wide retention policy, apply a retention period, and set the locations that the policy will be applied to.

1.  In **Microsoft Edge**, navigate to +++**https://compliance.microsoft.com+++** and log into the Microsoft Purview portal as **your created user account.**
2.  In the **Microsoft Purview** portal, in the left navigation pane, expand **Data lifecycle management** then select **Microsoft 365**.
3.  On the **Data lifecycle management** page, in the **Retention policies** tab select **+ New retention policy**.
4.  On the **Name your retention policy** page, for the **Name** and **Description** enter the following information:
    1.  **Name**: Company wide
    2.  **Description**: All locations except for teams
5.  Select the **Next** button.
6.  On the **Policy Scope** page select **Next**.
7.  In the **Choose the type of retention policy to create** area, select **Static** then select **Next**.
8.  In the **Choose where to apply this policy** enable:
    1.  **Exchange mailboxes**
    2.  **SharePoint classic and communication sites**
    3.  **OneDrive accounts**
    4.  **Microsoft 365 Group mailboxes & sites**
9.  Select **Next**.
10. On the **Decide if you want to retain content, delete it, or both** page, for the **Retain items for a specific period** section, enter the following information:
    1.  **Retain items for a specific period**: Choose **Custom** from the dropdown list
    2.  Change the years field to **3**
    3.  **Start the retention period based on**: When items were last modified
    4.  **At the end of the retention period**: Delete items automatically.
11. Select **Next**.
12. On the **Review and finish** page select **Submit**.
13. Once your policy is created select **Done**.

You have successfully created a retention policy for the Exchange email, Microsoft 365 groups, OneDrive, and SharePoint site’s locations. This retention policy will retain items in these locations for three years from when the item was last modified date. This policy can take up to 24 hours to be applied in your tenant, but you can proceed to the next step.

## Task 13: Assign Insider Risk Management Role

It is important to create an Insider Risk Policy in Microsoft Purview because it can help you to:

-   Identify and manage potential insider threats, such as data theft, data leakage, or security violations, by correlating various signals from user activities and behaviors.
-   Apply consistent and accurate sensitivity labels to your data assets automatically, based on the content and context of the data, using built-in or custom sensitive information types or trainable classifiers.
-   Enforce data protection policies and actions based on the sensitivity labels, such as encryption, access control, retention, and deletion.
-   Track and audit the usage and activity of your sensitive data across different sources and locations, such as Microsoft 365, SharePoint, OneDrive, Teams, Exchange, etc.
-   Comply with data privacy and security regulations and standards, such as GDPR, HIPAA, PCI DSS, etc.

You can create and manage Insider Risk Policies in the Microsoft Purview compliance portal², using a user-friendly interface that guides you through the policy creation process. You can also use PowerShell cmdlets or Graph APIs to create and manage Insider Risk Policies programmatically.

In this exercise, you will assign the Insider Risk Management role to Joni to grant access to perform insider risk tasks in the Microsoft Purview portal.

1.  In Microsoft Edge, navigate to +++**https://compliance.microsoft.com+++** and log into the Microsoft Purview portal as M365 Administrator ID provided by your lab hosting provider.
2.  Navigate to **Roles & scope**, then select **Permissions** from the dropdown.
3.  On the **Permissions** page, under **Microsoft Purview solutions** select Roles.
4.  On the **Role groups for Microsoft Purview solutions** page select **Insider Risk Management**.
5.  Select **Edit** from the **Insider Risk Management** flyout page on the right.
6.  On the **Edit members of the role group** page select **+ Choose users**.
7.  In the **Choose users** page select the check box next to Joni Sherman then select the **Select** button.
8.  On the **Edit members of the role group** page select **Next**.
9.  On the **Review the role group and finish** page select **Save**.
10. On the **You successfully updated the role group** page select **Done**.
11. Sign out of the **M365 Administrator** account and close all browser windows.

You have successfully assigned the Insider Risk Management role to Joni Sherman, granting her access to perform insider risk tasks in the Microsoft Purview portal.

## Task 14: Insider Risk Settings Configuration

In this task, you will customize the Insider risk management settings in the Microsoft Purview portal. This will allow your created user account to effectively manage potential insider risks within the organization and ensure the security of sensitive information.

1.  In **Microsoft Edge**, navigate to +++**https://compliance.microsoft.com+++** and log into the Microsoft Purview portal as user created user account.
2.  Select **Insider risk management** from the left navigation bar.
3.  Select the gear icon on the top right for **Settings**.
4.  Explore the settings:
    1.  **Privacy**: Allows you to select displaying usernames or anonymized versions in alerts and cases.
    2.  **Policy indicators**: Involves configuring the policy template using specific risk indicators.
    3.  **Policy timeframes**: Defines review periods triggered by policy matches based on events and activities.
    4.  **Intelligent detections**: Controls alert volume, excludes certain entities from risk scoring and allows filtering of Microsoft Defender alerts.
    5.  **Export alerts**: Exports risk alert information to SIEM and SOAR solutions using Office 365 Management Activity APIs.
    6.  **Priority user groups**: Determines high-risk users for closer inspection and more sensitive risk scoring.
    7.  **Priority physical assets (preview)**: Identifies and monitors access to priority physical assets correlating activity to user events.
    8.  **Power Automate flows (preview)**: Automates insider risk management tasks using Microsoft Power Automate flows.
    9.  **Microsoft Teams (preview)**: Enables Microsoft Teams for collaboration on insider risk management cases.
    10. **Analytics**: Assesses potential insider risks without configuring policies to guide policy creation.
    11. **Admin notifications**: Automatically sends email notifications to insider risk management role groups.
    12. **Inline alert customization**: Allows policy tuning and threshold adjustment directly from the Alerts dashboard.
5.  Select **Privacy** from the Insider risk management settings bar under **General**.
6.  Select **Do not show anonymized versions of usernames**.
7.  Select **Save** to save this setting.
8.  Select **Policy indicators** from the Insider risk management settings bar under **General**.
9.  On the **Policy indicators** settings pane, under **Office indicators** select the check box for **Select all**.
10. Scroll down and select **Save**.
11. Select **Priority user groups** from the insider risk management settings bar under **General**.
12. Select **+ Create priority user group** to open the **New priority user group wizard**.
13. On the **Name and describe the priority user group** page enter:
    1.  **Name**: Finance team
    2.  **Description**: Team members that manage financial operations, budgeting, and reporting
14. Select **Next**.
15. On the **Choose members** page select **+ Choose members**.
16. On the **Choose members** pane select the check box next to three random users then select **Add** to add 3 members.
17. On the **Choose members** page select **Next**.
18. On the **Choose who can view data involving users in this priority group** select **+ Choose users and role groups**.
19. On the **Choose users and role groups** page select the checkbox next to **Insider Risk Management** to add all members who have the Insider Risk Management role in Microsoft Purview the select **Add**.
20. On the **Choose who can view data involving users in this priority group** select **Next**.
21. On the **Review** page select **Submit**.
22. On the **Created priority user group** page select **Done**. This will take you back to the insider risk management settings page.
23. Select **Insider risk management** to navigate back to the main Insider risk management page.

You have successfully customized the Insider risk management settings. Now, your created user account has the necessary tools and capabilities to proactively identify and mitigate insider risks, safeguarding valuable data in the Microsoft Purview portal.

## Task 15: Insider Risk Policy Creation

In this task, you will configure a policy named 'Financial Data Protection' in Microsoft Purview to monitor and protect sensitive financial data access within the organization.

1.  Select **Insider risk management** from the left navigation bar.
2.  Select the **Policies** tab from the top navigation bar then select **+ Create policy**.
3.  On the **Choose a policy template** page select **Data leaks** then select **Next**.
4.  On the **Name your policy page** enter:
    1.  **Name**: Financial Data Protection
    2.  **Description**: Sensitive financial data access monitoring
5.  Select **Next**.
6.  On the **Choose users and groups** page, leave **Include all users and groups** selected, then select **Next**.
7.  On the **Decide whether to prioritize content page**, leave only **Sensitive info type** selected then select **Next**.
8.  On the **Sensitive info types to prioritize** page select **+ Add or edit sensitive info type**.
9.  In the **Add or edit sensitive info types** pane search for *bank* and select the check box next to **U.S. Bank Account Number** and **International Banking Account Number (IBAN)**. Next search for *credit* and select the check box next to **Credit Card Number** then select **Add** to add the 3 sensitive info types.
10. Back on the **Sensitive info types to prioritize** select **Next**.
11. On the **Decide whether to score only activity with priority content** page leave **Get alerts for all activity** selected, then select **Next**.
12. On the **Triggers for this policy** page select **User performs an exfiltration activity**.
13. Under **Select which activities will trigger this policy** select:
    1.  **Downloading content from SharePoint**
    2.  **Sending email with attachments to recipients outside the organization**
    3.  **Using a browser to upload files to the web**
    4.  **Sharing SharePoint files with people outside the organization**
    5.  **File copied to remote desktop session**

        **Note**: If you are unable to select policy triggers, you may have a tip to Turn on indicators. If this option is available, select **Turn on indicators**. On the **Choose indicators to turn on** pop up, click the check box next to **Select all** for **Office indicators** then select **Save**.

14. Select **Next**.
15. On the **Triggering thresholds for this policy** page select **Use default thresholds (Recommended)** then select **Next**.
16. On the **Indicators** page, select the drop down for **Physical access indicators** and deselect **Physical access after termination or failed access to sensitive asset** if selected then select **Next**.
17. On the **Detection options** page select **Select all** from the **Sequence detection**, **Cumulative exfiltration detection**, and **Risk score boosters** sections, then select **Next**.
18. On the **Decide whether to use default or custom indicator thresholds** page select **Default thresholds** then select **Next**.
19. On the **Review settings and finish** page, select **Submit**.
20. On the **Your policy was created** page select **Done**.
21. **Note:** As noted on this page, it may take up to 24 hours before policy matches will start showing up in the Alerts tab.

You have successfully created the 'Financial Data Protection' policy, which will help detect and prevent unauthorized access to sensitive financial information. Keep in mind that it may take up to 24 hours for policy matches to appear in the Alerts tab.

# Microsoft Defender for Cloud

Microsoft Defender for Cloud is a cloud-native application protection platform (CNAPP) that helps strengthen your security posture, enables protection against modern threats, and helps reduce risk throughout the cloud application lifecycle across multicloud and hybrid environments. Microsoft Defender for Cloud helps you raise your organization's security posture by enabling you to:

-   Incorporate good security practices early during the software development process, or DevSecOps. You can use features such as infrastructure-as-code security, code security guidance, and DevOps posture visibility to help keep cloud applications secure from the start.
-   Gain visibility into data assets across your organization, including on-premises, multi-cloud, and software-as-a-service (SaaS) sources. You can use features such as security posture monitoring, regulatory compliance, and attack-path analysis to proactively improve your cloud security posture.
-   Help prevent, detect, and respond quickly to threats. You can use features such as workload protection, vulnerability scanning, and integrated threat protection with SIEM and XDR to gain comprehensive multicloud protection across cloud apps, infrastructure, and data.

Microsoft Defender for Cloud is based on open standards and interoperable with other Decentralized Identity solutions. It is also integrated with other Microsoft security solutions, such as Microsoft 365 Defender, Defender 365, and Microsoft Sentinel. By using Microsoft Defender for Cloud, you can elevate your security posture and protect your data against risks.

In this lab, you are a Security Operations Analyst working at a company that implemented Microsoft Defender for Cloud. You need to respond to recommendations and security alerts generated by Microsoft Defender for Cloud. You're a Security Operations Analyst working at a company that is implementing cloud workload protection with Microsoft Defender for Cloud. In this lab, you'll enable Microsoft Defender for Cloud.

## Task 1: Access the Azure portal and set up a Subscription

In this task, you'll set up an Azure Subscription required to complete this lab and future labs in this section.

1.  Open the Microsoft Edge browser or open a new tab if already open.
2.  In the Edge browser, navigate to the Azure portal at (+++https://portal.azure.com+++).
3.  In the **Sign in** dialog box, copy, and paste in the tenant Email account for the admin username provided by your lab hosting provider and then select **Next**.
4.  In the **Enter password** dialog box, copy, and paste in the admin's tenant password provided by your lab hosting provider and then select **Sign in**.
5.  In the Search bar of the Azure portal, type *Subscription*, then select **Subscriptions**.
6.  Select the *"Azure Pass - Sponsorship"* subscription shown (or equivalent name in your selected language).
7.  **Note:** If the subscription is not shown, ask your instructor on how to create the Azure subscription with your tenant admin user credentials. **Note:** The subscription creation process could take up to 10 minutes.
8.  Select **Access control (IAM)** and then select **Add role assignment** from the *Grant access to this resource* box.
9.  Select the **Privileged administrator roles** tab and then select **Owner**. Select **Next** to continue.
10. Under the *Members* tab, select **+ Select members** and select the **M365 Administrator** account and select **Select** to continue.
11. Select **Review + assign** twice to assign the owner role to your admin account.

**Important:** These labs have been designed to use less than USD \$10 of Azure services during the class.

## Task 2: Create a Log Analytics Workspace

In this task, you'll create a Log Analytics workspace for use with Microsoft Defender for Cloud.

1.  In the Search bar of the Azure portal, type *Log Analytics workspaces*, then select the same service name.
2.  Select **+Create** from the command bar.
3.  Select **Create new** for the Resource group.
4.  Enter *RG-Defender* and select **Ok**.
5.  For the Name, enter something unique like: *uniquenameDefender*.
6.  Select **Review + Create**.
7.  Once the workspace validation has passed, select **Create**. Wait for the new workspace to be provisioned, this may take a few minutes.

## Task 3: Enable Microsoft Defender for Cloud

In this task, you'll enable and configure Microsoft Defender for Cloud.

1.  In the Search bar of the Azure portal, type *Defender*, then select **Microsoft Defender for Cloud**.
2.  On the **Getting started** page, under the **Upgrade** tab, make sure your subscription is selected, and then select the **Upgrade** button at the bottom of the page. Wait for the *Trial started* notification to appear, it takes about 2 minutes.
3.  **Hint:** You can click the bell button on the top bar to review your Azure portal notifications.
4.  **Note:** If you see the error *"Could not start Azure Defender trial on the subscription"*, continue with the next steps to enable all the Defender plans in Step 5.
5.  In the left menu for Microsoft Defender for Cloud, under the Management, select **Environment settings**.
6.  Select the **"Azure Pass - Sponsorship"** subscription (or equivalent name in your Language).
7.  Review the Azure resources that are now protected with the Defender for Cloud plans.
8.  **Important:** If all Defender plans are *Off*, select **Enable all plans** and then click **Save**. Wait for the *"Resource plan in subscription Azure Pass were saved successfully!"* notification to appear.
9.  Select the **Settings & monitoring** tab from the Settings area (next to Save).
10. Review the monitoring extensions. It includes configurations for Virtual Machines, Containers and Storage Accounts. Close the "Settings & monitoring" page by selecting the 'X' on the upper right of the page.
11. Close the settings page by selecting the 'X' on the upper right of the page to go back to the **Environment settings** and select the '\>' to the left of your subscription.
12. Select the Log analytics workspace you created earlier *uniquenameDefender* to review the available options and pricing.
13. Select **Enable all plans** (to the right of Select Defender plan) and then select **Save**. Wait for the *"Microsoft Defender plan for workspace uniquenameDefender were saved successfully!"* notification to appear.
14. **Note:** If the page is not being displayed, refresh your Edge browser and try again.
15. Close the Defender plans page by selecting the 'X' on the upper right of the page to go back to the **Environment settings**

## Task 4: Explore Regulatory Compliance

Regulatory compliance is important in Microsoft Defender for Cloud because it helps you meet the security and compliance requirements for your hybrid cloud environment. It shows you how well you are following the best practices and standards that you have applied to your subscriptions, such as PCI-DSS, ISO 27001, NIST 800-53, and more. It also gives you recommendations and insights on how to improve your compliance posture and reduce your risk factors. You can also download reports, set up alerts, and export your compliance data using Defender for Cloud.

In this task, you will review Regulatory compliance configuration in Microsoft Defender for Cloud.

1.  Under *Cloud Security*, select **Regulatory compliance** in the portal menu.
2.  Select **Manage compliance policies** on the toolbar.
3.  Select your subscription.
4.  Under *Policy settings*, select **Security policy** in the portal menu.
5.  Scroll down and review the "Industry & regulatory standards" available to you by default. Note that *ISO 27001* is now deprecated.
6.  Select **Add more standards** to add the updated ISO 27001:2013 regulatory standard.
7.  Select the **Add** button to right of *ISO 27001:2013*.
8.  A new page to assign the Azure Policy initiative opens. Confirm that your subscription is selected under *Scope* and click **Review and create**.
9.  Select **Create** to assign the Azure Policy initiative to your subscription.
10. Select Microsoft Defender for Cloud below the search box to return to the main blade.
11. **Note:** You might want to return later to *Regulatory compliance* to review the new standard controls and recommendations.

## Task 5: Mitigate security alerts

The ability to mitigate security alerts in Microsoft Defender for Cloud is important because it helps you to protect your resources from potential threats and reduce the impact of a breach. By mitigating security alerts, you can:

-   Identify and resolve the root cause of the suspicious activity that triggered the alert.
-   Prevent further damage or data loss by stopping the attacker's actions or blocking their access.
-   Harden your resources and prevent future attacks of the same kind by following the security recommendations.
-   Streamline your response process by using automated actions or logic apps.

In this task, you will load sample security alerts and review the alert details.

1.  Under *General*, select **Security alerts** in the portal menu.
2.  Select **Sample alerts** from the command bar. **Hint:** you may need to select the ellipsis (...) button from the command bar).
3.  In the Create sample alerts (Preview) pane make sure your subscription is selected and that all sample alerts are selected in the *Defender for Cloud plans* area.
4.  Select **Create sample alerts**.
5.  **Note:** This sample alert creation process may take a few minutes to complete, wait for the *"Successfully created sample alerts"* notification.
6.  Once completed, select **Refresh** to see the alerts appear under the *Security alerts* area.
7.  For the alerts that grabbed your attention, perform the following actions:
    1.  Select the alert, information about the alert should appear. Select **View full details**.
    2.  Review and read the *Alert details* tab.
    3.  Select the **Take action** tab or select the **Next: Take Action** button at the end of the page.
    4.  Review the *Take action* information. Notice the sections available to take action depending on the type of alert: Inspect resource context, Mitigate the threat, Prevent future attacks, Trigger automated response and Suppress similar alerts.

You can also use the Take action tab to inspect resource context, mitigate the threat, prevent future attacks, or trigger automated response.

## Task 6: Review the Secure Score

Defender for Cloud displays your score prominently in the portal. When you select the Secure score tile on the overview page, you're taken to the dedicated secure score page, where you'll see the score broken down by subscription. Select a single subscription to see the detailed list of prioritized recommendations and the potential effect that remediating them will have on the subscription's score.

Your secure score is shown in the following locations in Defender for Cloud's portal pages:

1.  Review the Secure Score on the tile on Defender for Cloud's **Overview** (main dashboard)
2.  Review the Secure Score on the dedicated **Secure score page** where you can see the secure score for your subscription and your management groups.
3.  Review the Secure Score at the top of the **Recommendations** page.

## Task 7: Enable data-aware security posture

Data-aware security posture is a feature of Microsoft Defender for Cloud that provides automatic discovery and evaluation of data sensitivity and exposure. It helps you to reduce risk to data and respond to data breaches.

Some of the benefits of using data-aware security posture are:

-   You can automatically discover sensitive data resources across multiple clouds, such as object stores and databases.
-   You can evaluate data sensitivity, data exposure, and how data flows across the organization.
-   You can proactively and continuously uncover risks that might lead to data breaches.
-   You can detect suspicious activities that might indicate ongoing threats to sensitive data resources.
1.  Navigate to **Microsoft Defender for Cloud \> Environmental settings**.
2.  Select the relevant Azure subscription.
3.  For the Defender CSPM plan, select the **On** status.
4.  If Defender CSPM is already on, select **Settings** in the Monitoring coverage column of the Defender CSPM plan and make sure that the Sensitive data discovery component is set to **On** status.
5.  Once sensitive data discovery is turned On in Defender CSPM, it will automatically incorporate support for additional resource types as the range of supported resource types expands.

**NOTE:** It takes up to 24 hours to see the results of a first discovery after enabling the feature.

Sensitive data threat detection is enabled by default when the sensitive data discovery component is enabled in the Defender for Storage plan.

## Task 8: Protect your APIs with Defender for APIs

Defender for APIs in Microsoft Defender for Cloud offers full lifecycle protection, detection, and response coverage for APIs. Defender for APIs helps you to gain visibility into business-critical APIs. You can investigate and improve your API security posture, prioritize vulnerability fixes, and quickly detect active real-time threats.

**To enable the Defender for APIs plan:**

1.  In Defender for Cloud, select **Environment settings**.
2.  Select the subscription that contains the managed APIs that you want to protect.
3.  In the APIs plan, select **On**. Then select **Save**.
4.  Select **Save**.

**Onboard APIs:**

1.  In the Defender for Cloud portal, select **Recommendations**.
2.  Search for *Defender for APIs*.
3.  Under **Enable enhanced security features**, select the security recommendation *Azure API Management APIs* *should be onboarded to Defender for APIs*.
4.  In the recommendation page, you can review the recommendation severity, update interval, description, and remediation steps.
5.  Review the resources in scope for the recommendations:
    1.  **Unhealthy resources:** Resources that aren't onboarded to Defender for APIs.
    2.  **Healthy resources:** API resources that are onboarded to Defender for APIs.
    3.  **Not applicable resources:** API resources that aren't applicable for protection.
6.  In *Unhealthy resources*, select the APIs that you want to protect with Defender for APIs.
7.  Select **Fix**.
8.  In Fixing resources, review the selected APIs, and select **Fix resources**.
9.  Verify that remediation was successful.

# Microsoft Sentinel

Microsoft Sentinel is a cloud-native solution that provides security information and event management (SIEM) and security orchestration, automation, and response (SOAR) capabilities. It helps you raise your organization's security posture by enabling you to:

-   Collect data at cloud scale across all users, devices, applications, and infrastructure, both on-premises and in multiple clouds.
-   Detect previously undetected threats and minimize false positives using Microsoft's analytics and unparalleled threat intelligence.
-   Investigate threats with artificial intelligence, and hunt for suspicious activities at scale, tapping into years of cyber security work at Microsoft.
-   Respond to incidents rapidly with built-in orchestration and automation of common tasks.

Microsoft Sentinel is based on open standards and interoperable with other Decentralized Identity solutions. It is also integrated with other Microsoft security solutions, such as Microsoft 365 Defender, Entra ID, and Defender for Cloud. By using Microsoft Sentinel, you can gain a bird's-eye view across the enterprise and protect your data against modern risks.

To use Microsoft Sentinel, you need the following requirements:

-   An active Azure subscription. If you don't have one, you can create a free account before you begin.
-   A Log Analytics workspace. This is where Microsoft Sentinel will store and analyze the data that it collects from various sources. You can create a new workspace or use an existing one.
-   The correct permissions to deploy and use Microsoft Sentinel. You need contributor permissions to the subscription in which the Microsoft Sentinel workspace resides. You also need either Microsoft Sentinel Contributor or Microsoft Sentinel Reader permissions on the resource group that the workspace belongs to. To install or manage solutions in the content hub, you need the Template Spec Contributor role on the resource group that the workspace belongs to.
-   Microsoft Sentinel is a paid service. You should review the pricing options and the Microsoft Sentinel pricing page before you start using it.

In this lab, you are a Security Operations Analyst working at a company that is implementing Microsoft Sentinel. You are responsible for setting up the Microsoft Sentinel environment to meet the company requirements to minimize costs, meet compliance regulations, and provide the most manageable environment for your security team to perform their daily job responsibilities.

## Task 1: Initialize the Microsoft Sentinel Workspace

In this task, you will create a Microsoft Sentinel workspace. A Log Analytics workspace is required for Microsoft Sentinel. This is where data is stored, retained, and analyzed for security value.

1.  Open the Edge browser.
2.  In the Edge browser, navigate to the Azure portal at +++https://portal.azure.com+++.
3.  Sign-in using the lab-provided credentials on the Resource tab.
4.  In the Search bar of the Azure portal, type *Sentinel*, then select **Microsoft Sentinel**.
5.  Select **+ Create**.
6.  The next page, **Add Microsoft Sentinel** to a workspace will display a list of available Log Analytics workspaces to add Microsoft Sentinel. Select the button to start the "Create Log Analytics workspace" process.

The Basics tab includes the following options:

-   Subscription
-   Resource Group
-   Name
-   Region

The Name will be the name of the Microsoft Sentinel workspace. The Microsoft Sentinel name will default to the Log Analytics Workspace Name. The Region is the location where ingested data is stored. The data location impacts data governance requirements. Workspaces can't move from region to region; you will need to recreate the workspace if the region option needs to be changed.

1.  Select the **Review + Create** button and then select the Create button.
2.  The "Add Microsoft Sentinel to Workspace" screen will now appear after you've completed the previous steps.
3.  Wait for the newly created "Log Analytics Workspace" to appear in the list. This operation could take a few minutes.
4.  Select the newly created Log Analytics workspace. And select the **Add** button.
5.  The new Microsoft Sentinel workspace is now the active screen. The Microsoft Sentinel left navigation has four areas:
-   General
-   Threat management
-   Content management
-   Configuration

The Overview tab displays a standard dashboard of information about the ingested data, alerts, and incidents.

1.  Navigate around the newly created Microsoft Sentinel workspace to become familiar with the user interface options.

## Task 2: Configure log retention

It is important to configure log retention for Microsoft Sentinel because it allows you to:

-   Keep your security data for as long as you need, according to your organizational and regulatory requirements. Different data types may have different retention periods, depending on their relevance and value. For example, you may want to keep security alerts for longer than performance metrics.
-   Reduce the cost of storing and analyzing large volumes of data in your Log Analytics workspace. By archiving older, less used data, you can save on storage and query costs, while still being able to access the data when needed.
-   Optimize your security operations and investigations by having the right data available at the right time. By setting appropriate retention and archive policies for your data, you can ensure that you have the most relevant and recent data in your interactive workspace, while still being able to retrieve historical data from your archive storage.

In this task, you will change the retention period for the SecurityEvent table.

1.  In Microsoft Sentinel, select the **Settings** option under the *Configuration* area.
2.  Select **Workspace settings**.
3.  In Log Analytics workspace, select the **Tables** option under the *Settings* area.
4.  Search and select the table **SecurityEvent**, and then select the ellipsis button (...).
5.  Select **Manage Table**.
6.  Select **180 days** for *Total retention period*. Notice that *Archive period* is only 150 days, since it uses 30 days from the (default) *Interactive retention*.
7.  Select **Save** to apply the changes.

## Task 3: Connect the Microsoft Defender for Cloud data connector

You are a Security Operations Analyst working at a company that implemented Microsoft Sentinel. You must learn how to connect log data from the many data sources in your organization. The organization has data from Microsoft 365, Microsoft 365 Defender, Azure resources, non-azure virtual machines, etc. You start connecting the Microsoft sources first.

Connecting the Microsoft Defender for Cloud data connector to Microsoft Sentinel provides you with the following benefits:

-   You can stream security alerts from Microsoft Defender for Cloud into Microsoft Sentinel, so you can view, analyze, and respond to Defender alerts, and the incidents they generate, in a broader organizational threat context.
-   You can synchronize the status of security alerts between Microsoft Defender for Cloud and Microsoft Sentinel, so that any changes made in one service are reflected in the other.
-   You can enable bi-directional sync to automatically close the original security alerts in Microsoft Defender for Cloud when you close the corresponding Microsoft Sentinel incidents that contain those alerts.
-   You can use Microsoft Sentinel's advanced capabilities, such as workbooks, analytics, hunting, and automation, to enhance your security operations and investigations based on Microsoft Defender for Cloud data.

In this task, you will connect the Microsoft Defender for Cloud data connector.

1.  In the Microsoft Sentinel left menus, scroll down to the *Content management* section and select **Content Hub**.
2.  In the *Content hub*, search for the **Microsoft Defender for Cloud** solution and select it from the list.
3.  On the *Microsoft Defender for Cloud* solution page select **Install**.
4.  When the installation completes select **Manage**
5.  **Note:** The *Microsoft Defender for Cloud* solution installs the *Microsoft Defender for Cloud* Data connector and an Analytic rule.
6.  Select the *Microsoft Defender for Cloud* Data connector and select **Open connector page**.
7.  In the *Configuration* section, under the *Instructions* tab, **select** the checkbox for the "Azure Pass - Sponsorship" subscription and slide the **Status** option to the right.
8.  **Note:** If it switches back to disconnected, please review the Learning Path 3, Exercise 1, Task 1 to assign the proper permissions to your account.
9.  The *Status* should be now **Connected** and "Bi-directional sync" should be *Enabled*.
10. Scroll down and under the *Create incidents - Recommended!* area, verify that *Create incidents automatically from all alerts generated in this connected service* is **Enabled**.

## Task 4: Connect the Azure Activity data connector

Connecting the Azure Activity data connector to Microsoft Sentinel provides you with the following benefits:

-   You can stream Azure Activity Log data into Microsoft Sentinel, so you can view, analyze, and respond to Azure subscription-level events that occur in your organization, such as Azure Resource Manager operational data, service health events, write operations taken on the resources in your subscription, and the status of activities performed in Azure.
-   You can use Microsoft Sentinel's advanced capabilities, such as workbooks, analytics, hunting, and automation, to enhance your security operations and investigations based on Azure Activity data.
-   You can correlate Azure Activity data with other data sources in Microsoft Sentinel, such as Microsoft Defender for Cloud, Azure Security Center, Azure AD Identity Protection, etc., to gain a broader organizational threat context and improve your detection and response capabilities.

In this task, you will connect the *Azure Activity* data connector.

1.  In the Microsoft Sentinel left menus, scroll down to the *Content management* section and select **Content Hub**.
2.  In the *Content hub*, search for the **Azure Activity** solution and select it from the list.
3.  On the *Microsoft Defender for Cloud* solution page select **Install**.
4.  When the installation completes select **Manage**
5.  **Note:** The *Azure Activity* solution installs the *Azure Activity* Data connector, 12 Analytic rules, 14 Hunting queries and 1 Workbook.
6.  Select the *Azure Activity* Data connector and select **Open connector page**.
7.  In the *Configuration* area under the *Instructions* tab, scroll down to "2. Connect your subscriptions...", and select **Launch Azure Policy Assignment Wizard\>**.
8.  In the **Basics** tab, select the ellipsis button (...) under **Scope** and select your "Azure Pass - Sponsorship" subscription from the drop-down list and click **Select**.
9.  Select the **Parameters** tab, choose your *uniquenameDefender* workspace from the **Primary Log Analytics workspace** drop-down list. This action will apply the subscription configuration to send the information to the Log Analytics workspace.
10. Select the **Remediation** tab and select the **Create a remediation task** checkbox. This action will apply the policy to existing Azure resources.
11. Select the **Review + Create** button to review the configuration.
12. Select **Create** to finish.

You are a Security Operations Analyst working at a company that implemented Microsoft Sentinel. You must learn how to connect log data from the many data sources in your organization. Finally, you connect a threat intelligence feed to enhance your ability to detect and prioritize known threats.

## Task 5: Creating an Analytics Rule

Analytics rules are features in Microsoft Sentinel that help security teams discover and respond to threats and anomalous behaviors across their environment. There are different types of analytics rules, such as:

-   Microsoft security rules: These rules automatically create Microsoft Sentinel incidents from the alerts generated in other Microsoft security solutions, in real time. You can use Microsoft security rules as a template to create new rules with similar logic.
-   Fusion rules: These rules use the Fusion correlation engine, with its scalable machine learning algorithms, to detect advanced multistage attacks by correlating many low-fidelity alerts and events across multiple products into high-fidelity and actionable incidents. Fusion is enabled by default.
-   Machine learning behavioral analytics rules: These rules are based on proprietary Microsoft machine learning algorithms, so you can't see the internal logic of how they work and when they run. They detect anomalous user and entity behaviors, such as abnormal logon patterns, suspicious resource access, or unusual network activities.
-   Threat intelligence rules: These rules take advantage of threat intelligence produced by Microsoft to generate high fidelity alerts and incidents with the Microsoft Threat Intelligence Analytics rule.
-   Scheduled query rules: These rules allow you to write custom queries in Kusto Query Language (KQL) to search for specific events or sets of events across your environment, alert you when certain event thresholds or conditions are reached, generate incidents for your SOC to triage and investigate, and respond to threats with automated tracking and remediation processes.

In this task, you will create an Analytics Rule.

1.  Select Analytics from the navigation menu.
2.  Select *Create incidents based on Microsoft Defender for Cloud* from the rule templates.
3.  Select **Create rule** in the connector information blade.
4.  In the Analytics rule wizard, select **Next: Automated response**, then select **Next: Review and create**.
5.  Select **save**.

## Task 6: Explore workbook templates

A Microsoft Sentinel workbook is a feature that helps you to visualize and monitor your data collected by Microsoft Sentinel, using interactive reports and dashboards. You can use workbooks to create custom queries, charts, tables, and maps based on your data sources, or use existing workbook templates that are available with packaged solutions or as standalone content from the content hub. Workbooks can help you to:

-   Gain insights into your security posture and operations across different data types and scenarios, such as Azure activity, Microsoft 365 audit logs, threat intelligence, analytics efficiency, etc.
-   Correlate and analyze data from multiple sources and locations, such as Microsoft security solutions, Azure services, Windows devices, third-party products, etc.
-   Detect and respond to threats and anomalous behaviors across your environment, using Microsoft Sentinel's advanced capabilities, such as analytics rules, hunting queries, automation playbooks, etc.

In this task, you will explore the Microsoft Sentinel workbook templates.

1.  Select **Workbooks** under the *Threat Management* left blade. The *Templates* tab is selected by default.
2.  Search for and select the **Azure Activity** template workbook. In the right pane, scroll down and select the **View template** button.
3.  Review the contents of the workbook. It shows insights of your Azure subscription operations by collecting and analyzing the data from the Activity Log.
4.  Close the workbook by selecting the **X** in the top-right corner.

## Task 7: Save and Modify a workbook template

In this task, you will save a workbook template and modify it.

1.  You should be back in the **Microsoft Sentinel - Workbooks - Templates** tab. Scroll down again and select the **Save** button for the *Azure Activity* workbook.
2.  Leave **East US** as the default value for *Region* and select **OK**.
3.  Select the **View saved workbook** button.
4.  Select **Edit** in the command bar to enable changes in the workbook.
5.  Scroll down to the *Caller activities over time* area, look at the color of the *Activities* column since we are going to format those columns. Select the **Edit** button below the grid.
6.  Select the **Column Settings** button, it is located to the right of the *Run Query* command bar. **Hint:** This button only appears if there is data from the KQL query.
7.  In the *Edit column settings* blade that appears, within *Columns* select **Activities**.
8.  Change the value for *Column renderer* to **Heatmap**. For *Color palette*, scroll down to select **32-color categorical**.
9.  Select **Save and Close**. Notice the change in the *Activities* column.
10. Select **Done Editing** at the bottom of the query (not the top menu).
11. Now select **Done Editing** at the top menu and select the **Save** icon.
12. Close the workbook by selecting the **X** in the top-right corner.

## Task 8: Create a hunting query

**Hunting** in Microsoft Sentinel is a process where security analysts proactively seek out undetected threats and malicious behaviors across their organization's data sources, using interactive queries, dashboards, and notebooks. Hunting in Microsoft Sentinel can help you to:

-   Gain insights into your security posture and operations across different data types and scenarios, such as Azure activity, Microsoft 365 audit logs, threat intelligence, analytics efficiency, etc.
-   Correlate and analyze data from multiple sources and locations, such as Microsoft security solutions, Azure services, Windows devices, third-party products, etc.
-   Detect and respond to threats and anomalous behaviors across your environment, using Microsoft Sentinel's advanced capabilities, such as analytics rules, automation playbooks, etc.

A **Hunt** in Microsoft Sentinel is a feature that allows you to conduct end-to-end proactive threat hunting in Microsoft Sentinel, using the Hunts tab. A Hunt can help you to:

-   Define a hypothesis based on specific MITRE techniques, potentially malicious activity, recent threats, or your own custom idea.
-   Use security-researcher-generated hunting queries or custom hunting queries to investigate your hypothesis across your data sources and locations.
-   Collect evidence, investigate user and entity behaviors, and annotate your findings using hunt-specific bookmarks.
-   Collaborate and document your findings with comments.
-   Act on your results by creating new analytic rules, new incidents, new threat indicators, and running playbooks.
-   Keep track of your new, active, and closed hunts in one place.
-   View metrics based on validated hypotheses and tangible results.

In this task, you will create a hunting query, bookmark a result, and create a Livestream.

1.  Select **Logs**
2.  Enter the following KQL Statement in the *New Query 1* space:
3.  **Important:** Please paste any KQL queries first in Notepad and then copy from there to the *New Query 1* Log window to avoid any errors.
4.  `let lookback = 2d; `
5.  `SecurityEvent `
6.  `| where TimeGenerated >= ago(lookback) `
7.  `| where EventID == 4688 and Process =~ "powershell.exe"`
8.  `| extend PwshParam = trim(@"[^/\\]*powershell(.exe)+" , CommandLine) `
9.  `| project TimeGenerated, Computer, SubjectUserName, PwshParam `
10. `| summarize min(TimeGenerated), count() by Computer, SubjectUserName, PwshParam `
11. `| order by count_ desc nulls last `
12. Review the different results. You have now identified PowerShell requests that are running in your environment.
13. Select the checkbox of the results that shows the *"-file c2.ps1"*.
14. In the middle command bar, select the **Add bookmark** button.
15. Select **+ Add new entity** under *Entity mapping*.
16. For *Entity* select **Host**, then **Hostname** and **Computer** for the values.
17. For *Tactics and Techniques*, select **Command and Control**.
18. Go back to the *Add bookmark* blade, and the select **Create**. We will map this bookmark to an incident later.
19. Close the *Logs* window by selecting the **X** in the top-right of the window and select **OK** to discard the changes.
20. Select your Microsoft Sentinel workspace again and select the **Hunting** page under the *Threat Management* area.
21. Select the **Queries** tab and then **+ New Query** from the command bar.
22. In the *Create custom query* window, for the *Name* enter **PowerShell Hunt**.
23. For the *Custom query* enter the following KQL statement:
24. `let lookback = 2d; `
25. `SecurityEvent `
26. `| where TimeGenerated >= ago(lookback) `
27. `| where EventID == 4688 and Process =~ "powershell.exe"`
28. `| extend PwshParam = trim(@"[^/\\]*powershell(.exe)+" , CommandLine) `
29. `| project TimeGenerated, Computer, SubjectUserName, PwshParam `
30. `| summarize min(TimeGenerated), count() by Computer, SubjectUserName, PwshParam `
31. `| order by count_ desc nulls last `
32. Scroll down and under *Entity mapping* select:
    1.  For the *Entity type* drop-down list select **Host**.
    2.  For the *Identifier* drop-down list select **HostName**.
    3.  For the *Value* drop-down list select **Computer**.
33. Scroll down and under *Tactics & Techniques* select **Command and Control** and then select **Create** to create the hunting query.
34. In the *"Microsoft Sentinel - Hunting"* blade, search for the query you just created in the list, *PowerShell Hunt*.
35. Select **PowerShell Hunt** from the list.
36. Review the number of results in the middle pane under the *Results* column.
37. Select the **View Results** button from the right pane. The KQL query will automatically run.
38. Close the *Logs* window by selecting the **X** in the top-right of the window and select **OK** to discard the changes.
39. Right-click the **PowerShell Hunt** query and select **Add to livestream**. **Hint:** This also can be done by sliding right and selecting the ellipsis **(...)** at the end of the row to open a context menu.
40. Review that the *Status* is now *Running*. This will be running every 30 seconds in the background and you will receive a notification in the Azure Portal (bell icon) when a new result is found.
41. Select the **Bookmarks** tab in the middle pane.
42. Select the bookmark you just created from the results list.
43. On the right pane, scroll down and select the **Investigate** button. **Hint:** It might take a couple of minutes to show the investigation graph.
44. Explore the Investigation graph just like you did a the previous module. Notice the high number of *Related alerts* for *WINServer*.
45. Close the *Investigation* graph window by selecting the **X** in the top-right of the window.
46. Hide the right blade by selecting the **\>\>** icon and then scroll right until you see the ellipsis **(...)** icon.
47. Select **Add to existing incident**. All the incidents appear in the right pane.
48. Select one of the incidents and then select **Add**.
49. Scroll left to notice that the *Severity* column is now populated with the incident's data.

## Task 9: Access the KQL testing area

KQL stands for Kusto Query Language, which is the language used in Microsoft Sentinel to perform search, analysis, write detection rules and visualize data in Workbooks. KQL is a powerful tool to explore your data and discover patterns, identify anomalies and outliers, create statistical modeling, and more. The query uses schema entities that are organized in a hierarchy similar to SQLs: databases, tables, and columns.

KQL is also used in other Azure services, such as Azure Data Explorer, Azure Monitor Logs, Azure Resource Graph and Azure Data Explorer. KQL is inspired by famed undersea explorer Jacques Cousteau (and pronounced accordingly \\"koo-STOH\\"), and it’s designed to help you dive deep into your oceans of data and explore their hidden treasures.

The best way to get started learning KQL is to use the Must Learn KQL learning modules at ++++https://aka.ms/MustLearnKQL++++

In this task, you will access a Log Analytics environment where you can practice writing KQL statements.

1.  Go to +++https://aka.ms/lademo+++ in your browser. Login with the M365 Administrator credentials.
2.  Close the Log Analytics video pop-up window that appears.
3.  Explore the available tables listed in the tab on the left side of the screen.
4.  In the query editor, enter the following query and select the **Run** button. You should see the query results in the bottom window.
5.  `SecurityEvent`
6.  Notice that you have reached the maximum number of results (30,000).
7.  Change the *Time range* to **Last 30 minutes** in the Query Window.
8.  Next to the first record, select the **\>** to expand the information for the row.

## Task 10: Run Basic KQL Statements

In this task, you will build basic KQL statements.

**Important:** For each query, clear the previous statement from the Query Window or open a new Query Window by selecting **+** after the last opened tab (up to 25).

1.  The following statement demonstrates the **search** operator, which searches all columns in the table for the value. In the Query Window enter the following statement and select **Run**:
2.  `search "new"`
3.  The following statement demonstrates **search** across tables listed within the **in** clause. In the Query Window enter the following statement and select **Run**:
4.  `search in (SecurityEvent,App*) "new"`
5.  Change back the *Time range* to **Last 24 hours** in the Query Window.
6.  The following statements demonstrate the **where** operator, which filters on a specific predicate. In the Query Window enter the following statement and select **Run**:
7.  **Important:** You should select **Run** after entering each query from the code blocks below.
8.  `SecurityEvent  `
9.  `| where TimeGenerated > ago(1h)`
10. **Note:** The *Time range* now shows *Set in query* since we are filtering with the TimeGenerated column.
11. `SecurityEvent  `
12. `| where TimeGenerated > ago(1h) and EventID == 4624`
13. `SecurityEvent  `
14. `| where TimeGenerated > ago(1h)`
15. `| where EventID == 4624  `
16. `| where AccountType =~ "user"`
17. `SecurityEvent  `
18. `| where TimeGenerated > ago(1h) and EventID in (4624, 4625)`
19. The following statement demonstrates the use of the **let** statement to declare *variables*. In the Query Window enter the following statement and select **Run**:
20. `let timeOffset = 1h;`
21. `let discardEventId = 4688;`
22. `SecurityEvent`
23. `| where TimeGenerated > ago(timeOffset*2) and TimeGenerated < ago(timeOffset)`
24. `| where EventID != discardEventId`
25. The following statement demonstrates the use of the **let** statement to declare a *dynamic list*. In the Query Window enter the following statement and select **Run**:
26. `let suspiciousAccounts = datatable(account: string) [`
27. `  @"NA\timadmin", `
28. `  @"NT AUTHORITY\SYSTEM"`
29. `];`
30. `SecurityEvent  `
31. `| where TimeGenerated > ago(1h)`
32. `| where Account in (suspiciousAccounts)`
33. **Tip:** You can re-format the query easily by selecting the ellipsis (...) in the Query window and select **Format query**.
34. The following statement demonstrates the use of the **let** statement to declare a *dynamic table*. In the Query Window enter the following statement and select **Run**:
35. `let LowActivityAccounts =`
36. `    SecurityEvent `
37. `    | summarize cnt = count() by Account `
38. `    | where cnt < 1000;`
39. `LowActivityAccounts | where Account contains "sql"`
40. Change the **Time range** to **Last hour** in the Query Window. This will limit our results for the following statements.
41. The following statement demonstrates the **extend** operator, which creates a calculated column and adds it to the result set. In the Query Window enter the following statement and select **Run**:
42. `SecurityEvent  `
43. `| where TimeGenerated > ago(1h) `
44. `| where ProcessName != "" and Process != "" `
45. `| extend StartDir =  substring(ProcessName,0, string_size(ProcessName)-string_size(Process))`
46. The following statement demonstrates the **order by** operator, which sorts the rows of the input table by one or more columns in ascending or descending order. The **order by** operator is an alias to the **sort by** operator. In the Query Window enter the following statement and select **Run**:
47. `SecurityEvent  `
48. `| where TimeGenerated > ago(1h) `
49. `| where ProcessName != "" and Process != "" `
50. `| extend StartDir =  substring(ProcessName,0, string_size(ProcessName)-string_size(Process)) `
51. `| order by StartDir desc, Process asc`
52. The following statements demonstrate the **project** operator, which selects the columns to include in the specified order. In the Query Window enter the following statement and select **Run**:
53. `SecurityEvent  `
54. `| where TimeGenerated > ago(1h) `
55. `| where ProcessName != "" and Process != "" `
56. `| extend StartDir =  substring(ProcessName,0, string_size(ProcessName)-string_size(Process)) `
57. `| order by StartDir desc, Process asc `
58. `| project Process, StartDir`
59. The following statements demonstrate the **project-away** operator, which selects the columns to exclude from the output. In the Query Window enter the following statement and select **Run**:
60. `SecurityEvent  `
61. `| where TimeGenerated > ago(1h) `
62. `| where ProcessName != "" and Process != "" `
63. `| extend StartDir =  substring(ProcessName,0, string_size(ProcessName)-string_size(Process)) `
64. `| order by StartDir desc, Process asc `
65. `| project-away ProcessName`

## Task 11: Analyze Results in KQL with the Summarize Operator

In this task, you will build KQL statements to aggregate data. **Summarize** groups the rows according to the **by** group columns, and calculates aggregations over each group.

1.  The following statement demonstrates the **count()** function, which returns a count of the group. In the Query Window enter the following statement and select **Run**:
2.  `SecurityEvent  `
3.  `| where TimeGenerated > ago(1h) and EventID == 4688  `
4.  `| summarize count() by Process, Computer`
5.  The following statement demonstrates the **count()** function, but in this example, we name the column as *cnt*. In the Query Window enter the following statement and select **Run**:
6.  `SecurityEvent  `
7.  `| where TimeGenerated > ago(1h) and EventID == 4624  `
8.  `| summarize cnt=count() by AccountType, Computer`
9.  The following statement demonstrates the **dcount()** function, which returns an approximate distinct count of the group elements. In the Query Window enter the following statement and select **Run**:
10. `SecurityEvent  `
11. `| where TimeGenerated > ago(1h)`
12. `| summarize dcount(IpAddress)`
13. The following statement is a rule to detect Invalid password failures across multiple applications for the same account. In the Query Window enter the following statement and select **Run**:
14. `let timeframe = 30d;`
15. `let threshold = 1;`
16. `SigninLogs`
17. `| where TimeGenerated >= ago(timeframe)`
18. `| where ResultDescription has "Invalid password"`
19. `| summarize applicationCount = dcount(AppDisplayName) by UserPrincipalName, IPAddress`
20. `| where applicationCount >= threshold`
21. The following statement demonstrates the **arg_max()** function, which returns one or more expressions when the argument is maximized. The following statement will return the most current row from the SecurityEvent table for the computer SQL10.NA.contosohotels.com. The \* in the arg_max function requests all columns for the row. In the Query Window enter the following statement and select **Run**:
22. `SecurityEvent  `
23. `| where Computer == "SQL10.na.contosohotels.com"`
24. `| summarize arg_max(TimeGenerated,*) by Computer`
25. The following statement demonstrates the **arg_min()** function, which returns one or more expressions when the argument is minimized. In this statement, the oldest SecurityEvent for the computer SQL10.NA.contosohotels.com will be returned as the result set. In the Query Window enter the following statement and select **Run**:
26. `SecurityEvent  `
27. `| where Computer == "SQL10.na.contosohotels.com"`
28. `| summarize arg_min(TimeGenerated,*) by Computer`
29. The following statements demonstrate the importance of understanding results based on the order of the *pipe*. In the Query Window enter the following queries and run each query separately:
    1.  **Query 1** will have Accounts for which the last activity was a login. The SecurityEvent table will first be summarized and return the most current row for each Account. Then only rows with EventID equals 4624 (login) will be returned.
    2.  `SecurityEvent  `
    3.  `| summarize arg_max(TimeGenerated, *) by Account `

        `| where EventID == 4624  `

    4.  **Query 2** will have the most recent login for Accounts that have logged in. The SecurityEvent table will be filtered to only include EventID = 4624. Then these results will be summarized for the most current login row by Account.
    5.  `SecurityEvent  `
    6.  `| where EventID == 4624  `

        `| summarize arg_max(TimeGenerated, *) by Account`

30. **Note:** You can also review the "Total CPU" and "Data used for processed query" by selecting the "Query details" link on the lower right and compare the data between both statements.
31. The following statement demonstrates the **make_list()** function, which returns a *list* of all the values within the group. This KQL query will first filter the EventID with the where operator. Next, for each Computer, the results are a JSON array of Accounts. The resulting JSON array will include duplicate accounts. In the Query Window enter the following statement and select **Run**:
32. `SecurityEvent  `
33. `| where TimeGenerated > ago(1h)`
34. `| where EventID == 4624  `
35. `| summarize make_list(Account) by Computer`
36. The following statement demonstrates the **make_set()** function, which returns a set of *distinct* values within the group. This KQL query will first filter the EventID with the where operator. Next, for each Computer, the results are a JSON array of unique Accounts. In the Query Window enter the following statement and select **Run**:
37. `SecurityEvent  `
38. `| where TimeGenerated > ago(1h)`
39. `| where EventID == 4624  `
40. `| summarize make_set(Account) by Computer`

## Task 12: Create visualizations in KQL with the Render Operator

In this task, you will use generate visualizations with KQL statements.

1.  The following statement demonstrates the **render** operator (which renders results as a graphical output), using a **barchart** visualization. In the Query Window enter the following statement and select **Run**:
2.  `SecurityEvent  `
3.  `| where TimeGenerated > ago(1h)`
4.  `| summarize count() by Account`
5.  `| render barchart`
6.  The following statement demonstrates the **render** operator visualizing results with a time series. The **bin()** function rounds all values in a timeframe and groups them, used frequently in combination with **summarize**. If you have a scattered set of values, the values are grouped into a smaller set of specific values. Combining the generated results and pipe them to a **render** operator with a **timechart** provides a time series visualization. In the Query Window enter the following statement and select **Run**:
7.  `SecurityEvent  `
8.  `| where TimeGenerated > ago(1h)`
9.  `| summarize count() by bin(TimeGenerated, 1m)`
10. `| render timechart`
