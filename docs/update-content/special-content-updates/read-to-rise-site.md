---
sidebar_position: 1
---

# Read to Rise Website

Read to Rise is built with READsquared software.

This document pertains to updating the content on the Read to Rise site. For details about READsquared system setup, see [READsquared System Setup Documentation](https://docs.google.com/spreadsheets/d/1kCVdKClzPiwuuzOSDoBAyf1i610POPWR2t5x4v2w2A4/edit?usp=sharing).

## Update the Featured Titles Widget

**Who:** Any staff with access to List Widgets in Catalog (the 5800 account)  
**Widget Name:** READsquared Read to Rise Widget - https://catalog.library.nashville.org/Admin/CollectionSpotlights?objectAction=view&id=337  
**Host Location:** Catalog  
**How to Update:** To swap out the titles in the Featured Titles widget, follow the directions below. You must have permissions in Pika to update catalog widgets. If you do not have access to this feature in Pika, contact Web Services for help.

1. Log in to Catalog (https://catalog.library.nashville.org) with the lists account.
1. Grab the list ID from the end of the list URL. For example, for https://catalog.library.nashville.org/MyAccount/MyList/39596, the ID is 39596.
1. Go to Pika Configuration > List Widgets and find the READsquared Read to Rise widget. Click Edit.
1. Scroll to the bottom of the widget form. Update the NAME field to display the name of the new list. Update the number in the SOURCE field to point to the new list, like this: list:39596
1. Click Save.
1. Go to https://library.nashville.org/readtorise and make sure the new list is showing in the widget area.

## Update the Literacy Tips

**Who:** Web Services  
**File Name:** literacy-tip-machine.js  
**Host Location:** hosted in the Bucket server at https://assets.library.nashville.org/js/literacy-tip-machine.js  
**How to Update:** To add/edit the literacy tips, update the JavaScript file on bucket.

1. Open Cyberduck.
1. Go to the bucket server.
1. Find literacy-tip-machine.js in the images folder. Open the file in Sublime text.
1. Add / Edit / Delete the tips in the array.
1. Save and push changes.
1. Double check that changes display on the Read to Rise site: http://npl.readsquared.com/Default.aspx?PID=459

## Add a New Activity Calendar

**Who:** Web Services  
**Host Location:** Activity calendars are hosted on Drupal. Just upload as a file to the website.  
**How to Update:** To add a new activity calendar, follow the instructions below. You must have permission to upload files to the website and have a READsquared account with permission to edit Programs.

1. Upload the file to the NPL site:
   1. Log in to the NPL website.
   1. Go to Content > Media > Add Media  File.
   1. Choose the file you want to upload.
      1. File should be a PDF with no spaces in the file name.
      1. Format the file with dashes and use all lowercase: read-to-rise-calendar-month-2020.pdf
      1. Name the file: Read to Rise Activity Sheet Month 2021
      1. Save.
   1. Go to Content > Files.
   1. Copy the URL for the PDF.
   1. Test the URL to make sure you can get to the newly uploaded file (and save that URL for the next step).

1. Add the link to the Activity Sheets page in READsquared:
   1. Log in to READsquared.
   1. Select Look and Feel > Custom Content.
   1. Click the edit button next to the Read to Rise Activity Calendars link.
   1. Click the Center Column box.
   1. Add the new calendar to the Activity Calendars list.
   1. Remove the oldest calendar link. We keep the current month and previous 6 months of activity calendars (for a total of 7).
   1. Save.

1. Review the changes on the live site and test the new link to verify it works.

## Get a READsquared Email Extract

**Who:** Read to Rise staff (Terri Thomas) and READsquared  
**Host Location:** READsquared

Need a report from the "Read to Rise" program that includes Child's First and Last Name, Parent's First and Last Name, email address, and the yes/no email toggle. At this time the Ad Hoc report does not include parent first/last name, so we have to contact READsquared to request the data. They will pull it for us.

After pulling the report, send it to MarCom.
