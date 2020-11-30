---
# This basic template provides core metadata fields for Markdown articles on docs.superoffice.com.

# Mandatory fields.
title: configure_video_meetings # (Required) Very important for SEO. Intent in a unique string of 43-59 chars including spaces.
description: How to configure video meetings in SuperOffice # (Required) Important for SEO. Recommended character length is 115-145 characters including spaces.
author: {github-id}             # Your GitHub alias.
keywords:
so.topic: howto             # article, howto, reference, concept, guide

# Optional fields. Don't forget to remove # if you need a field.
so.envir: cloud               # cloud or onsite
so.client: online             # online, web, win, pocket, or mobile
---

# How to configure video meetings in SuperOffice

To be able to send and receive email invitations to video meetings (to/from external users), you must have configured your email setup in SuperOffice CRM (user client) or use SuperOffice Mail Link.

## With SuperOffice Inbox

1. Configure your email setup in [SuperOffice Inbox][1].
2. To be able to send the Video Meeting URL to external users, we recommend to edit your invitation template][4] to add the new variable {burl}.

## With SuperOffice Mail Link

1. Set the [SuperOffice Mail Link][2] preference under "Invitations": 'Add / update appointments in SuperOffice...'

This feature is currently not supported if you use [Synchronizer for SuperOffice][3] - as they don't support this yet.

**Next step:** register video provider

<!-- Referenced links -->
[1]: https://community.superoffice.com/documentation/help/EN/CRM/9.2/UserHelp/StandardCRM/chap07web/Inbox_CRM_web.htm
[2]: https://community.superoffice.com/documentation/help/EN/CRM/9.2/UserHelp/index.htm#t=MailLink/topics/Introduction.htm
[3]: https://online.superoffice.com/appstore/infobridge-software-b-v-/synchronizer-for-superoffice
[4]: https://community.superoffice.com/documentation/help/en/crm/9.2/webhelpadmin/chap08/Add_e-mail_template.htm