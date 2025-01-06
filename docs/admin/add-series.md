---
Title: Adding a Topical Area
sidebar_position: 2
---

# Adding a Topical Area

You can’t really change a category. If you want to change a category you need to remove the old category and add a new category. If you remove a category it will affect old events, so keep that in mind.

## Add a Topical Area

1. Login to Bedework.
1. Under “choose your administrative group” click calsuite-MainCampus.
1. Create a category:
    1. Double check where you are. You should be on the “Main Menu” tab in “Group: calsuite-MainCampus.” Note: Follow the conventions of the existing categories - they are CASE SENSITIVE.
    1. Select Manage Categories.
    1. Click Add a New Category.
    1. Enter Keyword like this:  ‘series/Series Name’
    1. Enter description like this: ‘Series Name’
    1. Click “Add Category”

1. Create a new alias:
    1. Click the System tab.
    1. Click Manage Calendars & Folders.
    1. On the left, under the “Public Tree” heading, click the tiny + next to expand “aliases.
    1. On the left, under the “Public Tree” heading, click the tiny + next to expand whichever topical area you’re adjusting (location, topic, series).
    1. Click the Add icon to the right of the topical area category you’re adjusting (location, topic, series). For example, the add icon to the right of “Series.”
    1. Fill out the form:
       1. System Name: ‘Series Name’ (do NOT put the “series/” part here)
       1. Display Name: ‘Series Name’
       1. Description: ‘Series Name’
       1. Filter: Click the ‘show/hide categories for filtering on output’ button. Scroll down and click the checkbox next to the category you created earlier.
       1. Categories: Click the ‘show/hide categories for filtering on input’ button. Scroll down and click the checkbox next to the category you created earlier.
       1. Type: Select the radio button next to “Subscription.”
       1. URL to Calendar: Type “bwcal:///public/cals/MainCal” - This URL appears on the screen underneath this area – easy to cut & paste.
       1. Click “Add.”
       1. You should see your new topical area in the list on the left of this “manage calendars and folders” page.

1. Add a subscription (creating an alias to an alias):
    1. Change to the 'Calendar Suite' tab.
    1. Choose Manage Subscriptions.
    1. Click on the + icon to the right of “MainCampus” to expand the list. If you’re adding a series, click on the + icon to the right of “Series” to expand the list.
    1. Click on the add icon next to the topical area you are adjusting. For example, if you’re adding a new series, click the add icon next to series.
    1. Fill out the form:
       1. System Name: ‘Series Name’ (do NOT put the “series/” part here)
       1. Display Name: ‘Series Name’
       1. Description: ‘Series Name’
       1. Filter: Leave alone.
       1. Categories: Leave alone.
       1. Type: Public Alias should be selected. Click the “Select a public calendar or folder” button.
       1. Scroll down the list and click on the category/alias you created in step 2.
       1. Click on “Add.”
       1. Go to the Main Menu and click Add Event. Verify that you see the new topical area where expected.

1. Create a view (this makes the topical area show up in the public calendar):
    1. Change to the 'Calendar Suite' tab.
    1. Click “Manage Views”
    1. Click the view where you want your topical area to live. If you just added a series, click “series” in the list.
    1. On the view screen, find your topical area on the left (it will probably be black) and click on it to add it to the view on the right.

1. Check the public calendar.
    1. Refresh XSLT.
    1. See if the series is displaying.
