---
sidebar_position: 3
---

# Campaign Tagging

## Overview

### What is Campaign Tagging?

NPL shares links in email newsletters, on social media, and print materials. Emma or Instagram each have some kind of analytics tracking, but it’s difficult to compare engagement across mediums. And it is time consuming to pull together numbers into a single report. Campaign tagging allows us to track these interactions and pull together stats in one place.

Campaign tags are special query parameters that are added to the end of a web address shared on an external site (social media, newsletter, etc.). These tags override Google Analytics’ default detection of where a user comes from.

For example, when you look at Google Analytics reports for the NPL website, you can see the number of users who came to library.nashville.org from twitter.com. But you cannot tell whether users happened to visit library.nashville.org after visiting twitter.com, or if they clicked a link NPL posted on Twitter. Adding campaign tags changes that. If that same Twitter user clicks a tagged link, Google Analytics will recognize that a user came from Twitter using a link NPL shared.

### What Can We Get from the Data?

- See which source or medium got the most interaction. Did we get more website traffic from users who heard about us through print, email, or social media? Did Instagram paid ads do better than a post on Twitter?
- Do A/B testing and analyze what type of content is most effective at driving people to the content we want them to view. Do people respond better videos in an email? Or text/button calls to action?
- For vanity URLs in print media, we can get a sense of whether people are using the shortlinks they see in print or hear on the news. Are people memorizing that url - is it sticking?
- See stats for QR codes. Are people using the QR code? Do they tend to scan fliers or go right to unbound?

### Parts of a Campaign URL

- **utm_source** (required): Describes where the link lives. Identifies the specific source of the visitor, e.g. “salon+at+615+newsletter” or “twitter”.
- **utm_medium** (required): Describes how users reached your site. Identifies the broad category by which users reached your site, e.g. “email” or “referral”.
- **utm_campaign** (required): The marketing campaign the URL is associated with, e.g. “read+to+rise” or “be+well+at+npl+health+fair”. Campaign labels pull all the other labels together, identifying all the different mediums and sources you used for a particular purpose (product launch, event series, or an ongoing promotion).
- **utm_term** (optional): Used primarily for paid search, but we can use it as an extra spot to add parameters.
- **utm_content** (optional): A field to define more about the specific link, like its location or other relevant information not covered by the other parameters, e.g. “sidebar” or “cta+button”. You could compare how well different links perform within the same source, medium, or campaign. Which type of link persuades more people to click?

### Further Reading

- https://www.lunametrics.com/blog/2011/09/08/4-steps-campaign-data-google-analytics/
- https://www.lunametrics.com/blog/2016/04/11/naming-events-traffic-sources-google-analytics
- https://www.lunametrics.com/blog/2017/09/19/campaign-links-in-google-analytics/

## Tagging Guidelines

Campaign parameters should only be added to off-site links (social media, print, email) that point a user to an NPL site. Never tag internal links (links on NPL, Limitless, Catalog, Salon, Events, or other NPL websites) with campaign parameters.

- Use the [Campaign Tracking Worksheet](http://bit.ly/npl-ga-campaign-worksheet) to build campaign URLs.
- Check the Master Tag List tab for the correct source and medium terminology.
Use lowercase for all parameters. Parameters are case sensitive. Tagging something with “Email+Newsletter” is not the same as tagging it “email+newsletter”. Stick to lowercase all the time for consistency.
- Use **+** to separate terms. Google Analytics translates + into a space. So, “email+newsletter” displays as “email newsletter” in GA reports.
- Use **%2D** to separate parts of a date -> %2D will display as a - in reports.
- Format dates as **yyyy**%2D**mm**%2D**dd**.
- Only add dates to the utm_content field, like adding the date to the newsletter.
- If you must add additional punctuation to a URL (like parentheses or a slash), use this guide to find additional [encoding symbols](https://www.w3schools.com/tags/ref_urlencode.asp): https://www.w3schools.com/tags/ref_urlencode.asp
      - Example Name: Out of Print Master Engaged Segment - 120 days (no purchases after 8/31)
      - Encoded Name: Out+of+Print+Master+Engaged+Segment+-+120+days+%28no+purchases+after+8%2F31%29

## Campaign Tagging Process

Note: Campaign tagging is for links that *point to* the website. Never add campaign parameters to a link that *lives* on the NPL site (a link in a home promo, on a basic page, etc.) or you will wreck our data.

### Plan Upcoming Campaigns

1. Identify the opportunities to track for each campaign: newsletter, twitter, facebook, instagram, etc.
1. Identify the landing page(s) where you want to send users.
1. Determine if you need a vanity URL. If yes, contact Web Services.

### Make Campaign URLs

Put all tags in the Tracking Worksheet so you can double check each other’s syntax, keep track of tags from previous campaigns, and stay organized.

1. Open the [Campaign Tracking Worksheet](http://bit.ly/npl-ga-campaign-worksheet). If you need a new tab/sheet, make a copy of the Master Sheet and rename the new tab.
1. Use the tagging spreadsheet to create a tagged-URL (fill out columns C - L). Use one line for each opportunity you’re tracking.
1. Copy and paste the automatically generated campaign URL from column L into a new browser to make sure it works.
1. Double check the list of campaign URLs as a group to make sure there are no syntax errors.
1. Take the tagged URL from column L and create a bit.ly link. You must make the bit.ly link from the tagged URL from column L.
1. Paste the bit.ly link in column M.
      1. This helps keep all the bit.ly links straight so you don’t use a link in the wrong place.
      1. You can make all your bit.ly links in one sitting, then come back and grab the right one when you actually make the post or email or QR code.
1. Note in column N the date the bit.ly link was created. We’re trying this field for now, but we can lose this column later if it doesn’t turn out to be useful.  
1. Remember: Never add campaign parameters to a link that lives on the NPL site (a link in a home promo, on a basic page, etc.) or you will wreck our data.


### Using a QR Code

1. Open up the Open the [Campaign Tracking Worksheet](http://bit.ly/npl-ga-campaign-worksheet), because this is where you stashed your bit.ly links.
1. Create a QR code using the bit.ly link saved in column M. You must make the QR code with the bit.ly link!
      1. The bit.ly link contains the tagged-URL.
      1. The bit.ly link will make a much prettier / easier to scan QR code.
1. IF QR CODE: Save the QR code file in the correct folder on Z > Communications.
1. IF QR CODE: Note the folder path to the QR code in column O, like this: Z > Communications > [folder name] > [folder name] > filename.jpg
      1. Everyone will know where to find the QR code for a specific piece of collateral.
      1. You won’t get QR codes mixed up (you’ll know which is the bookmark QR code vs which is the poster QR code).
1. IF QR CODE: Share the print-ready QR code file with whoever needs it.  
1. Remember: Never add campaign parameters to a link that lives on the NPL site (a link in a home promo, on a basic page, etc.) or you will wreck our data.

### Use the Campaign Links

Add the campaign-tagged links to messages we’re sending out: email, twitter, etc.

1. Open the [Campaign Tracking Worksheet](http://bit.ly/npl-ga-campaign-worksheet), because this is where you stashed your bit.ly links.
1. Copy/paste the bit.ly links into emma, hootsuite, etc.
1. Remember: Never add campaign parameters to a link that lives on the NPL site (a link in a home promo, on a basic page, etc.) or you will wreck our data.

### Get Data from Google Analytics

1. Log in to [Google Analytics](https://analytics.google.com/analytics/web/).
1. Select the property where users were being sent (NPL site, Calendar, Catalog, etc.)
1. Click on Acquisition > Campaigns > All Campaigns
      1. Campaigns will be listed by the value entered in utm_campaign.
      1. You will be able to see sessions, users, pages viewed per session, and average session duration. You will not see conversion data unless/until we set up goals.
1. Click on Acquisition > Source / Medium
      1. Source / Medium will be listed by the value entered in utm_source and utm_medium.
      1. You will be able to see how many sessions we got from each source / medium, etc.

## Demonstration

See the [Campaign Tagging presentation](https://docs.google.com/presentation/d/1gpEPYTKbwNhUpbDbms1AUTQFuxwplSxU/edit?usp=sharing&ouid=100711184815519661331&rtpof=true&sd=true) for an overview with slides.
