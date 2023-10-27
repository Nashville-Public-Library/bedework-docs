---
title: Troubleshooting
---

# Troubleshooting

## About Master and Instance Listings

Ellis thinks this:
-	If instances are exception instances, updates to the master will NOT update the instance.
-	If the instances are normal instances, updates to the master WILL update each instance.

Cook thinks this:
-	If instances are added with dates (not pattern), updates to the master will NOT update the instance.
-	If instances are added with pattern, updates to the master WILL update each instance.
Are both of the above true?
## Editing Recurrences / Master and instances

-	If master is added with dates (not pattern), using the second Recurrence option on the form, future updates to the master will NOT update the instance. (Not sure if this is how it actually works, but this behavior doesn’t seem correct. If this is busted, this may be a change that needs to happen to the whole Project.)
-	If instances are added with pattern (every Tuesday, until apr 12), updates to the master WILL update each instance. (Yes, these are true.)
-	After individual instance is updated, so it now differs from the Master, changes to the Master WILL NOT affect this instance. (Yes, these are true.)
-	Role shouldn’t affect any behavior. Should be separate from role.
## Disappearing Events

If an event is not visible in either the public client or the admin client, we need to report to Bedework Vendor.

1. [Reindex Bedework](../admin/reindex.md).
1. Report to Bedework vendor if a reindex doesn't make the event surface.

## Bedework Widget Malfunctioning (but site is fine)

Display of events is happy (calendar is working), but the feed might be unhappy.

1.	Look and see if widgets are busted EVERYWHERE or just in specific sites / instances (check all npl site pages, salon, nashville reads, digital signs).
    1. [https://library.nashville.org/](https://library.nashville.org/)
    1. [https://library.nashville.org/event/be-well-npl](https://library.nashville.org/event/be-well-npl)
    1. [https://library.nashville.org/locations/main-library](https://library.nashville.org/locations/main-library)
    1. [https://library.nashville.org/income-tax-help](https://library.nashville.org/income-tax-help)
    1. [http://nashvillepubliclibrary.org/nashvillereads/events/](http://nashvillepubliclibrary.org/nashvillereads/events/)
    1. [http://nashvillepubliclibrary.org/salonat615/](http://nashvillepubliclibrary.org/salonat615/)
    1.	With image signs:
        1.	http://firesign.library.nashville.org/MN_moviesAtMain.htm
        1.	http://firesign.library.nashville.org/MN_courtyardconcerts.html
    1.	No image signs:
        1. [http://firesign.library.nashville.org/BL_NovelConversations.html](http://firesign.library.nashville.org/BL_NovelConversations.html)
        1.	[http://firesign.library.nashville.org/GO_PageTurners.html](http://firesign.library.nashville.org/GO_PageTurners.html)
        1.	[http://firesign.library.nashville.org/MN_killerthrillers.html](http://firesign.library.nashville.org/MN_killerthrillers.html)
    1.	Restart Bedework.
    1.	Report to Bedework vendor, if restart doesn’t fix widgets. Report where widgets are malfunctioning.

When we upgraded to 3.10, URLs changed. Bedework Vendor wrote a translator to that read old-style-urls and changed them to new-style-urls. Look to see if we are using any old style links:
-	Old style - webcache
-	New style - feeder or vfeeder
2020: reviewed code and it looks like we are NOT using any old style widgets.

## Emergency Restart

1. Notify Shared Systems, Bedework Application Admin, then Back-up staff.
1. Login to server via ssh. `sudo reboot`.
- If this fails, contact Bedework Vendor.
- Post a note to the Intranet notifying staff that the events calendar is down and we are working on it.
- If the calendar is affecting the home page, replace the homepage calendar feed with an alternate box (we’d need to come up with some kind of alternate content and add it to the page code, commented out).
- Once calendar is back up:
    -Post a note to the Intranet notifying staff.
    - Reinstate the home page calendar feed and comment out the replacement box.

1.	Past errors:
    1.	`Service Temporarily Unavailable
> The server is temporarily unable to service your request due to maintenance downtime or capacity problems. Please try again later.`
`Apache/2.2.3 (Red Hat) Server at events.library.nashville.org Port 80`

Info: Bedework Vendor had a backup file saved somewhere and Bedework was trying to load two files at once. For some reason it started causing problems one day. He removed the backup file and the calendar was fine.`

## Event Stuck in Approval Queue

Events stuck in approval queue that don’t really exist.

1.	[Reindex Bedework](../admin/reindex.md).
1.	Test.
1.	If event is still in the database, and it is a master event, open the master event, then clear the recurrence pattern and reset it. Save the master event. Find the event in Bedework admin console and try to delete an instance again.
1.	If the event is still stuck, notify Bedework Vendor.
