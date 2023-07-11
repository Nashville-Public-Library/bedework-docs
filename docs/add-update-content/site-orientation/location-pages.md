---
sidebar_position: 2
---

# Location Pages

Each individual location page is made with the branch content type.

## Manager, Hours, Closures

### Update Manager

The manager is pulled in from the list of person nodes.

#### Update the person node.

1. Go to content.
1. Search for a person by first or last name. If there is no person node, you need to create one. See: *Add Content with Components* for adding specific types of content: https://nashville-public-library.github.io/website-guide/docs/add-update-content/site-orientation/person/
1. Select 'edit' next to the person you need to upgrade to manager or downgrade.
1. Update staff info.
   1. If the staff person is a new manager, make the following updates:
      1. Set 'department' to 'branch.'
      1. Update phone number, if needed.
      1. Update location, if needed.
      1. Update job title, if needed.
      1. Go to 'staff directory settings' and check the box next to 'list in the directory.'
   1. If the staff person used to be a manager and moved into a non-manager job, make the following updates:
      1. Update department, if needed.
      1. Update phone number, if needed.
      1. Update location, if needed.
      1. Update job title, if needed.
      1. Go to 'staff directory settings' and UNcheck the box next to 'list in the directory.'
   1. If the staff person left NPL, make the following updates:
      1. Change 'department' to none.
      1. Remove job title, email, and phone.
      1. Update 'blog bio' to reflect that the staff person is no longer at NPL.
      1. Go to 'staff directory settings' and UNcheck the box next to 'list in the directory.'
1. Save.

#### Update the Location Page

1. Go to the location page.
1. Click edit.
1. On the 'contact info' tab, update the name under 'branch manager' by selecting a name from the dropdown.

### Closure Notices

In the "Hours" tab, each branch has a field for "Extended Closure" that is used whenever the branch is closed for multiple days.

1. Go to the locations page.
1. Select the location you need to update.
1. Click Edit.
1. Select the "Hours" tab.
1. Scroll to the bottom of the hours listing and find the "Extended Closure" field.
1. Type a message in the field. This message will be displayed two places:
   1. Closure message will replace the hours block on the locations landing page.
   1. Closure message will replace the hours block on the individual branch page.

## Amenities List

Amenities are created with a view. To update an amenity listing for a branch, you must edit the branch page.

### Update Amenities List

1. Go to the locations page.
1. Select the location you need to update.
1. Click Edit.
1. Select the "Branch Details" tab.
1. Update the amenities for the location by checking and unchecking boxes by each amenity.
1. Save.
1. Review the page to make sure updates are correct.

## Branch Description and Calendar

We use the Two Column component to set up a container that is divided into two columns. One column is about 2/3 wide and the other is about 1/3 wide.
- Branch description: Contained in the 2/3 column. Text is added with components.  
- Calendar: Contained in the 1/3 column. Calendar is added with the calendar widget component (the Attend an Event option).
