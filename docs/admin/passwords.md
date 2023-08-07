---
title: Users and Passwords
---

# Users and Passwords
Adding users to Events is a two step process. The admin client doesn't know anything about what you're doing in the jmx-console.

It's the difference between authentication (which is whether you can log in or not) and authorization (whether you allowed to administer the system). The jmx-console is handling authentication. Adding users to the superuser list or adding them to an admin group handles authorization.

 Add them in the jmx-console and then visit the admin client and add them to an admin group.

Deleting users cleanly is also a two step process. If you succeed in removing the user in the jmx-console, then the user won't be able to log in at all. So, you've removed a user via the jmx-console, they'll be shut out of the system. To keep things orderly, remember to remove the user from Bedework Users groups as well.
## User Creation / Management Checklist
Use this checklist when adding/editing/removing users from the JMX Console, Events, and Steven:
<<<<<<< HEAD
```
https://metronashville.sharepoint.com/:x:/r/sites/NPLWebDevelopment/Shared%20Documents/Bedework%20Staff%20Submitters%20Account%20Creation%20_%20Management%20Checklist.xlsx
```
=======
[Bedework Staff Submitters Account Creation Checklist](https://metronashville.sharepoint.com/:x:/r/sites/NPLWebDevelopment/Shared%20Documents/Bedework%20Staff%20Submitters%20Account%20Creation%20_%20Management%20Checklist.xlsx)
>>>>>>> bf29c59
## JMX Console Functions
### Access jmx-console:

1.	The jmx console is now located at: https://events.library.nashville.org/hawtio/login
1.	Log in with:
1.	Click on `JMX` on LHS
1.	Click on `>` next to `org.bedework.selfreg`
1.  Choose `config`
1.	Click `Operations` from the tabs
### Check if user exists in db

1. To list a user, click on `displayUser`. Type in account name in Account box. Click `Execute`
### Reset Password

1.	Click `setUserPassword` and fill out the field.
1.	Click `Invoke`.
### New User

1.	Click `addUser` and fill out 5 fields:
    1. Account (username)
    1. First Name
    1. Last Name
    1. Email 1
    1. Password
## CalAdmin User Functions

1.	Go to https://events.library.nashville.org/caladmin
1.	Select correct calSuite.
### Grant User Permissions

Now that user is added, you have to give user permissions:

1.	Go to `Users` tab.
1.	Click `Manage Admin Groups`.
1.	Click setting to `show members` at the top.
1.	Select `membership` next to the correct group.
1.	In `add member` box, you can add users and groups. Make sure box is selected for “user” > type username > and click Add.
### Designate Users as Approvers

1.	Go to Users tab.
1.	Click Manage Admin Roles.
1.	Click “edit” next to anyone we want to make an approver.
1.	Select checkbox next to Approver.
1.	Select Done.
1.	Approvers MUST be in the group for which they’ll be approving events. Don’t forget to add Approvers to groups.