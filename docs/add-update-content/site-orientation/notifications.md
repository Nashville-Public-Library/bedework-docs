---
sidebar_position: 1
---

# Notifications (Alerts)

## About

Drupal 8 has two types of notices: Site Wide and Contextual. The major difference is where the alert is displayed. That condition is determined by which alert you select and the settings you define in the Notification Conditions section.

Drupal 8 also has extended closure notices on each location page. Type a message to replace the branch hours with a notice.

## Showing/Hiding the “Read More” Button

| Desired Result                                    | “Message” Field                     | “Read More URL” Field                                           |
|---------------------------------------------------|-------------------------------------|-----------------------------------------------------------------|
| No “Read More” Button                             | Add content to the “Message” field. | Leave “Read More URL” field blank.                              |
| Read More Button --> Notification Page            | Add content to the “Message” field. | Leave “Read More URL” field blank.                              |
| Read More Button --> Drupal page or External page | Leave “Message” field blank.        | Add a URL to the “Read More URL” field. Can be a relative path. |

## Add a Site Alert (Yellow Bar at Top of Website)

A site alert is shown site-wide in the yellow bar at the top of the website.

1. Go to Content > Notification Message.
1. Select Add Notification Message.
1. Select Site Alert.
1. Fill out the form:
   1. Label: Displays in the admin UI and as the page title in the browser tab. Does not display to the user on the actual webpage.
   1. Headline: Displays as the alert text in the yellow bar at the top of every page on the site.
   ![home page components](/img/site-orientation-13.png)
   1. Read More URL (optional):
      1. If the alert points to a specific blog post or website, put that link here. You must include the full URL, not a relative path.
      1. If the Read More URL is left blank, the user will be taken to the notification page and will see content added to the Message field.
   1. Message (optional): Displayed to the user only if they click the “read more” link.
      1. More Info on Notification Page: Add the notification content to the message field. You must leave the “Read More URL” blank for the user to go to the notification page.
      1. More Info on External or Other Drupal Page: Add the “Headline” text to the message field. Put a full URL in the “Read More URL” field
      1. No Read More Link: Leave the “Message” field is left empty. Do not add a “Read More URL” link. The alert will show only the headline.
   1. Notification Conditions: Ignore for site wide alerts.
   1. Notification Options: Schedule your alert (message publish) or change authoring information (message information).
      1. Message Publish: Select the start and end date for your alert.
      ![home page components](/img/site-orientation-14.png)
      1. Message Information: Do not change unless absolutely necessary.
1. Select time period the notification will be active.
1. Save.

## Add a Contextual Alert (Specific Page/Content Type)

A contextual alert is shown on individual pages or types of content. For example, you can post a contextual alert to a single database page (if ABC-CLIO is broken) or an alert to one or more branch pages (if we’re paving driveways and want to alert visitors).

1. Go to Content > Notification Message.
1. Select Add Notification Message.
1. Select Site Alert.
1. Fill out the form:
   1. Label: Displays in the admin UI and as the page title in the browser tab. Does not display to the user on the actual webpage.
   1. Headline: Displays as the alert text in the yellow bar above the content on a specific page. The example below is on the ABC-CLIO database page.
   ![home page components](/img/site-orientation-15.png)
   1. Read More URL (optional): Displayed to the user only if they click the “read more” link.
      1. If the alert points to a specific blog post or website, put that link here. You must include the full URL, not a relative path.
      1. If the Read More URL is left blank, the user will be taken to the notification page and will see content added to the Message field.
   1. Message (optional): Displayed to the user only if they click the “read more” link.
      1. More Info on Notification Page: Add the notification content to the message field. You must leave the “Read More URL” blank for the user to go to the notification page.
      1. More Info on External or Other Drupal Page: Add the “Headline” text to the message field. Put a full URL in the “Read More URL” field
      1. No Read More Link: Leave the “Message” field is left empty. Do not add a “Read More URL” link. The alert will show only the headline.
   1. Notification Conditions: Set the context for your alert.
      1. Content Type: Displays an alert on all pieces of a specific type of content, like all databases or all internship opportunity posts. Select the Content Type tab, then check the box for the specific type of content you want to target.
      1. Node Bundle: Ignore. Same as Content Type.
      1. NPL Branch: Displays an alert on one or more location pages. Select the NPL Branch tab, then check the box next to the branch(es) that should display the alert.
      1. Request Path: Displays an alert on one or more pages based on URL. For example, you could post an alert on the ABC-CLIO database only (rather than all databases) by putting the ABC-CLIO URL in the “pages” field.  
      1. Current Theme: Ignore.
   1. Notification Options: Schedule your alert (message publish) or change authoring information (message information).
      1. Message Publish: Select the start and end date for your alert.
      ![home page components](/img/site-orientation-14.png)
      1. Message Information: Do not change unless absolutely necessary.
1. Select time period the notification will be active.
1. Save.

## Edit Existing Notifications

1. Log in to the web site at https://library.nashville.org/user with your username and password.
1. Go to Content > Notification Message
1. You should see a list of notifications. Select Edit next to the notification. Or use the dropdown arrow to delete an alert.
![home page components](/img/site-orientation-16.png)
1. Make your changes and save. Your alert will only be visible to users if you update the publish start and end dates.
![home page components](/img/site-orientation-17.png)
1. Save your changes.

## Add Extended Closure Notice

[See Closure Notice info on Locations page](http://localhost:3000/website-guide/docs/site-orientation/location-pages/#closure-notices) for step-by-step.

## Add Alert to Catalog

### Catalog (NPL or School)

1. Log in to the catalog: https://catalog.library.nashville.org
1. Click on “hamburger menu” to the right of your account name.
Select Aspen Administration.
1. In the LOCAL CATALOG ENRICHMENT section, select System Messages.
1. Select Add New or edit an existing message.
   1. Add New > Click Add New button:
      1. Title: Type the title of the alert that is visible in the admin view.
      1. Message to Show: Type the message visible to patrons.
      1. Show On: Select the places to show the message.
      1. Message Style: Select warning (yellow).
      1. Start Date to Show: Select the date the message will publish.
      1. End Date to Show: Select the date the message will unpublish.
      1. Dismissible: Check the box if you’d like the alert to be dismissable.
      1. Libraries: Select MNPS for school catalog. Select NPL for library catalog. Select both boxes if the message is the same for both systems.
      1. Locations: For Aspen System Messages to show up on in-branch OPAC screens (and public internet terminals browsing to catalog.library.nashville.org), the branch must be selected in the Locations list for the system message. I.e., it's probably best that, when posting a message to Aspen, you select All Libraries and All Locations.
   1. Edit Existing > Click edit button.
1. Scroll to the bottom of the page, click ‘Save Changes and Return.’
1. Go to catalog.library.nashville.org or school.library.nashville.org and verify changes are visible and correct.
