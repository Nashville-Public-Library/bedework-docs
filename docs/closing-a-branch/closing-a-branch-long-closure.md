---
sidebar_position: 3
---
# Closing a Branch for Several Weeks / Months (Planned Closures)

Use this guide to update NPL website properties for planned closures lasting more than one week.

## As Soon As Closing is Confirmed (2-4 Weeks Prior to Closing)

### LibCal  

#### Update Branch Hours in LibCal (LibCal)
1. Log in to LibCal.  
1. In the Admin menu (gear icon), select Hours: https://nashvillepl.libcal.com/admin/hours   
1. Find the branch whose hours are changing. Click the "Edit Hours" link.  
![Edit Hours](/img/libcal-1.jpg)  
1. In the lightbox, you'll see a list of hours with a start date and end date. Update the end date to be the day before the closure. Pay close attention to the year! Then click "Update."  
![Edit Hours](/img/libcal-2.jpg)  
1. Add a new line for hours. Use the date of the closure for start and end dates. Set the template to "fully closed."  
![Edit Hours](/img/libcal-3.jpg)  
1. Add a new line for hours. Use the day *after* the closure date for the start date. This is the first day the branch will be open following the closure. Set the end date to Dec 31, 2037. Use the same hours template from the original hours list. In our example, it's the 30 Min Open Close template for regional branches. Click Add.   
![Edit Hours](/img/libcal-4.jpg)  
1. Verify in the hours preview (top of the hours lightbox) that everything looks okay for the duration of the closure.  

#### Mark Meeting Rooms Unavailable During Closure (LibCal)
Branch managers will make the following updates:  
- Required: Cancel any events already scheduled in meeting rooms and notify the person who booked the room about the cancelation.
- Optional: Block of meeting room space for the days their branch is closed. This is not strictly necessary. Updating the location hours will automatically remove the meeting room booking options for the days closed.  

#### Remove Appointment Availability / Cancel Appointments (LibCal)
Book a Librarian staff will make the following updates:  
- Required: Cancel or reschedule all confirmed appointments.
- Required: Remove staff person's appointment availability from LibCal for the period of the branch closure.

## On the Closure Date  

### Add Contextual Alert to the Branch Location Page (Drupal)  

MarCom will add a site alert to the library website and library catalog. Shared Systems adds an alert to update the locations page.  

1. Go to 'Content' > 'Notification message.'  
1. Choose 'Add a notification message' > 'Contextual Alert'  
1. Use 'Headline' field to help identify the nature of the closure for other website editors. This field will not display to the public.  
1. In 'Message' box, note the date of the closure, and when branch is set to reopen.  
1. In 'Notification Conditions,' choose 'NPL Branch,' and relevant location.  
1. In 'Message Publish' set the dates we want to display the alert on the location page; can be scheduled in advance.  

### Update Hours on Website Locations Page (Drupal)  

We add an extended closure notice to hide the normal operating hours.   

1. Go to the locations page.  
1. Select the location to update.  
1. Edit the hours tab.  
1. In 'Extended Closure' box, note the date of the closure, and when branch is set to reopen.  
1. Save.  

### Disable Remote Printing (Shared Systems)  

1. Go to the mobile printing page: https://library.nashville.org/services/mobile-printing-instructions
1. Edit the page and comment out the branch that will be closed. This will hide the branch printing email so that users cannot easily send a print job to the closed location. Be sure to comment out *all* places on the page where the branch is mentioned.   
1. Save the page. Verify that the branch name and/or printing email is not visible on the page.
1. Make a Trello card to un-comment out the branch on the printing page once the branch reopens.

### Bedework
See instructions for [Cancel or Reschedule](https://nashville-public-library.github.io/bedework-guide/docs/admin/cancel/)

### Google, Yelp, Apple Maps, Etc.

#### Google
We update Google Maps when a branch is closing for more than a week, or when operating hours have changed.
1. Go to [Google Business Profile](https://business.google.com/)
1. Click Sign In.
   1. Enter the login info for NPL's Google account.
1. You should see a list of all of NPL’s business listings on a page called 'Google Business Profile Manager.
1. Click on the pencil icon in the row of the location.

#### Bing Places
We update Bing Places when a branch is closing for more than a month, or when opening hours have changed.
1. Go to [Bing Places for Business](https://bingplaces.com)
1. Login using credentials from passwd repo
1. From dashboard, choose location.
1. On left-menu, choose 'Add Special Hours'

#### Yelp
We update Yelp when a branch is closing for more than a month, or when opening hours have changed.
1. Go to [Yelp for Business](https://biz.yelp.com). Login using credentials from password repo.
1. Choose location from drop-down, then 'General Information'
1. Update hours using 'Hours of Operation' and 'Special Hours' interfaces. 'Special Hours' allows us to close for multiple days, as in an extended closure.

#### Apple Maps
Yelp currently populates hours for Apple Maps (used by iPhone users). No separate steps needed.

## Holidays

### Google Holidays Hours

We can update the holidays hours for all locations using the export spreadsheet feature.
1. Select all locations with the box at top of table. A menu will appear.
1. Download the .csv or .xlsx from 'export'
1. Made adjustments to every cell in the column for 'closed dates' to match our upcoming holidays.
1. Import updated file to Google from same menu.

### LibCal Holidays
