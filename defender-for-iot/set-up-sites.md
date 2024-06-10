---
title: Set up a new site for Site security for Microsoft Defender for IoT in XDR Defender portal
description: This article describes the set-up procedure for a new site in the Site security feature of Microsoft Defender for IoT in XDR Defender portal
ms.service: defender-for-iot
author: lwainstein
ms.author: lwainstein
ms.localizationpriority: medium
ms.date: 05/19/2024
ms.topic: how-to
---

# Set up a new site for Site security/ Defender for IoT?

In this article, you learn how to set up a new site in the Site security dashboard. Microsoft Defender for IoT uses *sites* to group Operational Technology (OT) devices located at a specific physical location, such as an office or factory building. The Site security dashboard allows the security site management team an overview of the most important security issues affecting your network to make quick, highly informed decisions about which security problems need an immediate response.

Defender for IoT uses the MDE agent to identify and locate other OT and IoT devices at the same location. Defender for IoT adds these devices to the Device inventory, so it's recommended that you know the IP address of at least one OT device.

## Prerequisites

- Review [the general prerequisites needed for Microsoft Defender for IoT](prerequisites.md).
- OT Security Admin with MDE P2/E5. For more information, see [Microsoft Defender for Endpoint subscriptions settings](/defender-endpoint/defender-endpoint-subscription-settings.md).
- Microsoft Defender for IoT license with at least one site license available. For more information, see [Microsoft Defender for IoT subscriptions settings](license-admin-center.md).
- We recommend you have IP or MAC address details of at least one OT device at the site.

## Set up a new site

1. In the Site security dashboard, select **Create new site** or **Create Your First Site**.

1. Enter the following details:

- Site name - a name for the site, for example, San Franscico Main office.
- Location - the physical location of the office.
- Site description - describe the purpose of the site, what activities occur there, the types and number of devices used, and other important information about the site.
- Owners - the contact emails of any users administering the site, who must be contacted when problems occur.

    :::image type="content" source="media/site-security-set-up-details.png" alt-text="Screenshot showing the details for a new site in the Site security page of Microsoft Defender for IoT in the Microsoft Defender portal.":::

1. When completed, select **Next**.

## Associate devices

OT devices are associated with the site allowing Microsoft Defender for IoT to correctly identify other OT/IoT devices at the same site.

1. In the Search bar, type either a public IP address or the IP/MAC address for a specific OT device that is located at this site. A list of suggested sites appears in the table.
    1. If you don't know any of the OT device addresses, select **Show all suggested sites**, and a list of all possible sites appears in the table.

    Each row in the table is a suggested location based on the OT devices found there. Open the location to see the list of OT devices identified there, and check to see which devices exist at your site. You should look through each location, as Defender for IoT could find your OT devices in more than one suggested locations. You can't edit the list of devices at a location.

    1. Review the devices and select the rows to be added to your site. You might need to choose more than one item.

    :::image type="content" source="media/site-security-associate-devices.png" alt-text="Screenshot showing the associate devices screen and the suggested list of OT devices per location in the site set-up page of Microsoft Defender for IoT in the Microsoft Defender portal.":::

1. Select **Next**.

## Review site details

1. Review that information for the site you want to create.

    If you want to review the selected OT devices, select **Edit devices** and you return to the **Associate devices** screen.

    You have the option to create a Device group now or finish the site set-up. A Device group can also be set up at a later stage or it might need to be created by a different team member. For more information, see [add a device group](#add-device-group).

1. Select **Complete**.

The site is now set up and appears in the Site security page.

:::image type="content" source="media/site-security-dashboard-with-new-site.png" alt-text="Screenshot showing the newly added site in the Site security dashboard of Microsoft Defender for IoT in the Microsoft Defender portal.":::

## Add device group

A device group can be made using the link at the end of the Site set up process, or set up at another time.

Create a device group based on a site location to restrict users to that specific site. [ OR ]

It's important that only the correct users have access to the site. Access and permission controls can be set for groups of users to restrict access to a specific site or group of sites. Create a **Device group** and set the access per user.

1. Select **Create device group**. The Settings > Endpoints > Device groups page opens.
1. Select **Add device group**.
1. Type a **Device group name**.
1. Select the **Remediation level**.
1. Type a **Description**.<!-- optional -->
1. Select **Next**. The Devices page opens.
1. Type the value for the **Tag** condition. Type the term **Site:** and then the name of the site. For example, Site: San Francisco.
1. Select **Next**. The Preview devices page opens.
1. The Preview devices page displays a list of devices so that you can ensure you're creating the correct group. Select **Next**. The User access page opens.
1. Filter the user groups or choose the user groups to add to the device group.
1. Select **Submit**. The device group is created.
1. Select **Done**.
<!-- do we need an image of any of the above stages? -->
Your device group is now set up and appears in the Device group list.

Device groups might list different preferences for the same user, in which case you need to rank the importance of each Device group.

To move a group up or down, drag that row to the correct position in the list. For more information, see [ranking device groups in Microsoft Defender for Endpoint](/defender-endpoint/machine-groups.md).

To get the full benefit of the Device group, you might need to create roles and permission settings. For more information, see [role based access control in Microsoft Defender for Endpoint](/defender-endpoint/rbac.md).
Also see [create and manage roles in Microsoft Defender for Endpoint](/defender-endpoint/user-roles.md).
<!-- Or this link /defender-endpoint/user-roles.md , which is better? Site security and RBAC - Mia -->

## Next steps

Information about ranking
