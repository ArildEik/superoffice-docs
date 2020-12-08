---
# This basic template provides core metadata fields for Markdown articles on docs.superoffice.com.

# Mandatory fields.
title: migration_guide       # (Required) Very important for SEO. Intent in a unique string of 43-59 chars including spaces.
description: Migrate to SuperOffice CRM Online # (Required) Important for SEO. Recommended character length is 115-145 characters including spaces.
author: {github-id}             # Your GitHub alias.
keywords:
so.topic: guide                # article, howto, reference, concept, guide

# Optional fields. Don't forget to remove # if you need a field.
so.envir: onsite              # cloud or onsite
# so.client:                    # online, web, win, pocket, or mobile
---

# Migrate to Online

If you want to migrate to CRM Online you should contact your SuperOffice sales person, who will help you start the process.

The migration process must be initiated by your SupeOffice sales representative since all migrations will involve SuperOffice Online Operations. The sales representative will enlist a responsible technical consultant that will execute the migration (Migrator).

> [!CAUTION]
> If you have customizations or integrations, these may not be working after the migration. Check with the customization or integration developer if they have this available for CRM Online too, or check if the [App Store][1] have an app you may use instead.

## Customer service mailboxes

If you have Customer Service and want to migrate your data to our cloud we will create new email addresses for you.

**Why?**

Our cloud solution uses its own email service. This provides your company with your own new email addresses. Your new SuperOffice domain name will be based on your company name:

 ![x][3]

### How does this affect your company?

Simple! You will have to choose between have two alternatives:

* Keep the old email addresses and set up email forwarding to the new email address
* Use the new email addresses generated by SuperOffice

### If you want to keep your old email addresses?

No problem! But if you want to keep the old email addresses you will need to set up forwarding from your old email address to the new address generated by SuperOffice. Contact your current email provider to setup this. To learn how to find your new SuperOffice email addresses: [SuperOffice Mailboxes][4]

Also! If you choose to use your old email addresses, you might need to add an [SPF Record][5].

**Why?**

The purpose of an SPF record is to prevent spammers from sending messages with forged From addresses at your domain. Without the SPF record you risk having some emails from your customers ending up as spam.

**How?**

To add the SPF record, forward this information to your domain provider and refer to the following SPF (TXT) record:

```text
v=spf1 include:_spf.online.superoffice.com ~all
```

## Downtime during migration

You will have some downtime during the migration, the time depends on how large the database and document archive is.

## Before you migrate

### Your onsite SuperOffice version

You need to be on at least version 7.1 to migrate to CRM Online. If you run an older version of SuperOffice than 7.1, then an upgrade must be performed first.

### SuperOffice Admin check

The migrator needs access to SuperOffice administration client with a user with SuperOffice administrative rights.

Before migrating you will need to go through the following steps in the administration client:

* Make sure no users have duplicate email addresses:

 ![duplicate][2]

* Make sure all the users who should have access to SuperOffice Online have a license & a valid email address
* Make sure there are no users currently on Travel
* Make sure that you do not use SuperOffice Satellite and have active satellites

## Running the Online Migration Tool

The SuperOffice CRM Online Migration Tool (OMT) is responsible for transferring a local onsite database and document archive to online.  It also makes sure that a set of initial configuration steps are carried out.

The OMT can be executed in one of two basic modes:  Initial upload or recovery mode.

The OMT will automatically determine the mode when it starts.

![1.png][6]

The first step of the OMT is to log on to the local CRM onsite database.  The OMT will try to find a local windows installation.  It will then use that configuration and prompt the user with a user-name and password.  This must be the credentials of a local administrator (User or General Admin) in the CRM Database.

 ![2.png][7]

Contact details of the person performing the migration must be provided.  This is the contact details used during the migration process.

 ![3.png][8]

All users that shall log in to the migrated customer tenant in SuperOffice CRM Online must have a valid user license.  They must also have a valid e-mail address for logging in.  This e-mail address must be unique.  No other user can have the same e-mail address as such conflict will prevent successful logins to the system.

Both user plans and e-mail address user names must be validated by the migrator before the the customer can be migrated to online.

 ![4.png][9]

A new window is shown when the user clicks Check user plans.  The objective of this window is to ensure that all users that should have a valid user plan for log in, has this.

Each column represents a user plan.  The first column represents no user plan and users in this column are not allowed to log in.  At least one administrator must have a valid user plan.  Administrators are tagged with a golden crown.

 ![5.png][10]

Drag the user to the correct column to choose user plan.  Write a filter criteria to easier find a particular user or group of users.  All fields shown on the card is used in the free-text filter.  Filtering on name of user-group or position can be an efficient way of working with many users.

 ![6.png][11]

Click OK when licenses are assigned.  It is possible to come back to re-assign licenses after the other configuration steps are performed as well.

A valid e-mail address must be selected as user name.  All users must have a unique e-mail address.  Select one of the users existing e-mail addresses or write a new address as appropriate.

 ![blobid7.png][12]

If another user has user name e-mail address populated on his person card on the time of migration, it will be removed.

Filtering works the same way as on the user plan assignment page

 ![blobid8.png][13]

Click OK when all users are assigned a valid user name e-mail address

![blobid9.png][14]

Continuing the wizard will upload database and documents SuperOffice CRM Online.

It is quite common that some documents are missing during the time of migration.  When the documents are found, they can be put into the document archive and uploaded again.  Restarting the OMT will initiate the recovery process uploading missing document files

![blobid10.png][15]

Log on to the local database in the same way as a regular migration

![blobid11.png][16]

Missing documents will then be uploaded

![blobid12.png][17]

Close the OMT when the client-side of migration has completed.

![blobid13.png][18]

<!-- Referenced links -->
[1]: http://online.superoffice.com/appstore
[2]: https://community.superoffice.com/contentassets/8584441d96724f47b510db1b40b8032c/mig_proc_duplicate.jpg
[3]: https://community.superoffice.com/globalassets/technical-club/images/email-address-conversion.jpg
[4]: https://community.superoffice.com/en/customer/learn/settings-maintenance/service/inquiry/how-to-setup-mailboxes-for-superoffice/
[5]: https://support.google.com/a/answer/33786?hl=en
[6]: https://community.superoffice.com/contentassets/7a15f2d58a84479082f038d3a59183f3/1.png
[7]: https://community.superoffice.com/contentassets/7a15f2d58a84479082f038d3a59183f3/2.png
[8]: https://community.superoffice.com/contentassets/7a15f2d58a84479082f038d3a59183f3/3.png
[9]: https://community.superoffice.com/contentassets/7a15f2d58a84479082f038d3a59183f3/4.png
[10]: https://community.superoffice.com/contentassets/7a15f2d58a84479082f038d3a59183f3/5.png
[11]: https://community.superoffice.com/contentassets/7a15f2d58a84479082f038d3a59183f3/6.png
[12]: https://community.superoffice.com/contentassets/7a15f2d58a84479082f038d3a59183f3/blobid7.png
[13]: https://community.superoffice.com/contentassets/7a15f2d58a84479082f038d3a59183f3/blobid8.png
[14]: https://community.superoffice.com/contentassets/7a15f2d58a84479082f038d3a59183f3/blobid9.png
[15]: https://community.superoffice.com/contentassets/7a15f2d58a84479082f038d3a59183f3/blobid10.png
[16]: https://community.superoffice.com/contentassets/7a15f2d58a84479082f038d3a59183f3/blobid11.png
[17]: https://community.superoffice.com/contentassets/7a15f2d58a84479082f038d3a59183f3/blobid12.png
[18]: https://community.superoffice.com/contentassets/7a15f2d58a84479082f038d3a59183f3/blobid13.png