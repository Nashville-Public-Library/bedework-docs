---
sidebar_position: 2
---

# Database Pages

## Add a New Database

Use the database content type to add a new database to the site.

Fill out the form.

1. Title: Add the title of the resource.

1. Learn More Link Text: This affects the link text on the database cards on the Databases A-Z landing page and anywhere we show a database swim.
   1. Leave blank if you want the link text to be "Access" (this should be the default most of the time).
   1. Enter link text if you need the "Access" button to have different text. For example, we use "Register Now" instead of "Access" for the Ready Rosie database.

1. Feature Block: This is the block at the top of each database page with the image, tags, and brief description.
   1. Database Image: Square logo image.
      1. Width: 600px
      1. Height: 600px
   1. Description: Brief description.
      1. Max-characters: 170
   1. Database Link: URL for the resource.

1. Page Content: Add additional page content as needed.
   1. Access/Restrictions: Put any special access requirement here.
   1. Content: Add content components for instructions, video, or other information to aid in using the resource.

1. Tagging: Add audience and topic tags for the resource.

1. Links: Add help links or app download links.

## Remove a Database from the Site

### Initial Step

When we stop offering a database or product, patrons may still look for it on our site for a while. This procedure will help alert patrons to a service change.

1. Get whatever language we need to use to say “we’re not offering this anymore”.

1. Confirm with property-owner that this is indeed a dead service.

1. Edit the database node:
   1. Remove tags.
   1. Swap out database description with the “we’re getting rid of this” language.
   1. Remove content from all other fields (Access/Restrictions, Instructions, Check Out Periods, Contact).
   1. Remove Access link
   1. Remove “Get Help” and “Download the App” links

1. Do a site search on the NPL and LL sites to see where the resource is mentioned.
   1. Ignore blog posts b/c the redirects will take care of users looking at an old blog post.
   1. Update any mentions of the resource on major pages (like remove “ancestry” from the Special Collections page).

1. Remove database from EZProxy - Alert Shared Systems that the resource is going away.

1. Remove database from Pika - Alert Shared Systems that the resource is going away.

1. Alert any departments that may provide access to the resource (for example, for Ancestry, we needed to make sure Special Collections computers didn’t have a shortcut, etc.).

1. Find out if there is an email address related to the service. If yes, alert the program manager as a courtesy.

1. If the service had a subdomain or purchased domain name, see Domain Name Procedures for “Retiring a Domain Name.”

1. **Important!** Add a meeting request in Outlook for 3-6 months in the future.

### 3-6 Months After Unpublishing

After 6 months, redirect the page for the database that is going away. **The example below is for BoomBox (retiring) and Hoopla (keeping)**.

1. Un-publish the database we're retiring:
   1. In Content, find the database node for the database we’re retiring (BoomBox).
   1. Make a note of the current URL alias and jot it down in a notepad for later.
   1. Edit the node.
   1. Add “Retired” to the title field. Uncheck the box next to “publish.”
   1. Save.

1. Redirect the retired database's original URL alias.
   1. Go to the URL Redirects admin page: /admin/config/search/redirect
   1. Click “Add URL Redirect.”
   1. In the "path" field, enter the original URL alias path. In our BookBox example, you'd enter /research/databases/boombox as the original path because that's the original URL alias.
   1. In the "to" field, enter the path where you want the original URL alias to point. In our BoomBox example, we want the old BoomBox URL to go to the Hoopla page, so we'd enter /research/databases/hoopla.
   1. Save.
   1. If you get an error, go to Redirects to see if there’s already a redirect or an alias that’s preventing you from redirecting the database URL to the new destination.
      1. If there's an existing redirect, edit the existing redirect to point them to the new path.
   1. Clear cache.
   1. Test.

1. Alert MarComm that the resource is no longer offered and that we’ve updated the site (as a courtesy).
