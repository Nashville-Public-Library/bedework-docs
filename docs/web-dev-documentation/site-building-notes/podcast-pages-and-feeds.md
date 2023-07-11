---
sidebar_position: 2
---

# Podcast XML Feed View Creation in D8/D9

## Description of Content

### XML Feed

Generated with a view. Used a contextual filter so we could add podcasts without having to update or add a new view.

URL Structure: /podcasts/[term-id]/feed.xml

View was built by pulling in information from the podcast content type.

### Landing Page

URL Structure: /podcasts

For each series, collect the following information via the content type:
- Show logo
- Title
- Summary
- Series Landing Page - Term page DONE

URL Structure: /podcasts/podcast-series-name
- Top section (about the series)
   - Series Logo
   - Series Title
   - Series Description
   - Subscription buttons
   - Hosts
- Bottom section (list of all episodes - view block). For each episode, list the following:
   - Episode title
   - Date
   - Episode Summary

### Episode Pages

URL Structure: /podcasts/series-name/episode-title

For each episode, list the following:
- Episode title
- Audio (mp3 player)
- Date
- Series Tag (link to Podcast Series landing page)
- Episode Notes - content from the body field
- Subscribe buttons (referenced from the taxonomy term)
- Download button (save mp3 to device)
- Episode summary - summary for teaser or meta info

Notes:
- Episode number (removed field from form) - if you want an episode number, add it to the title
- Transcript - added field, but hid for now - we could show as a tab, like here: https://www.wnycstudios.org/podcasts/scattered/articles/cuckoos-nest

## How We Built It

### Podcast Series Pages (term pages)

Podcast series pages are taxonomy term pages.

"Hosted by" is rendered as label so that name displays but is not linked. If we want to make “host name” a link later, we can.

### Podcast Episode Pages

Podcast episodes are made with the podcast content type.

"Hosted by" is rendered as label so that name displays but is not linked. If we want to make “host name” a link later, we can.

### Podcast Subscription Links

In Structure > Taxonomy > Podcast Series:
- Added fields for each subscription service (Apple Podcasts, Spotify, etc.) to the Podcast Series vocabulary.

In Structure > Views > Podcast Subscribe Links:
- Created a taxonomy term view called Podcast Subscribe Links.
- Added a contextual filter for “Taxonomy term: Term ID” so we could pass in the value of the taxonomy term and know what podcast series we’re looking at.
- Added a header to the view so that an H2 displays showing “Listen for Free” above the subscribe links.
- Added fields for each of the subscription links from the Podcast Series vocabulary.
- Configured each field in the view with the following settings:
   - URL only - check this box
   - Show URL as plain text - check this box
   - Rewrite Results > Override the output of this field with custom text - check this box and type the service name in the text field (type Apple Podcasts for the Apple link)
   - Rewrite Results > Output this field as a custom link - check this box and enter the replacement pattern for the service url.
   - Rewrite Results > External Server URL - check this box
- Set the “no results behavior” to “hide if empty” so we wouldn’t show services we aren’t using.

In Structure > Content Types > Podcast Episode:
- Added a Viewfield field called field_subscribe_links.
- Set the default value to the Podcast Subscribe Links view.
- Added an argument for [node:field_podcast_series:target_id]. When a user is on a podcast episode, that episode is tagged with a podcast series term. That term will get passed to the Podcast Subscribe Links view.
- The view included at the end of each podcast episode node will show only those subscribe links that have content and that relate to the term referenced.

In Structure > Taxonomy > Podcast Series:
- Added a Viewfield field called field_subscribe_links, just like in the Podcast Episode content type. Did this so both the series and episode pages would be showing the same view for subscribe links. Thought it might make styling easier.
- Hid the individual subscribe links from view on manage display.

### Podcast RSS Feed

Podcast Module Notes:
- Module allows you, all of the properties are mapped to fields, module allows you to add fields you need for mapping.
- Module has src plugins:
   - Src > Plugin > row
   - Src > Plugin > style

Setting Up the view:
- Format: Podcast RSS Feed | Settings (use to do the mapping for feed) - these are all the fields the apply to the podcast series. Called the “channel.” Title here would be title for podcast series.
- Show: Podcast Fields | Settings (use to do the mapping for episodes) - these are all the fields that apply to the podcast episode itself. Called the “items.” Title in this case would be title for episode.
- Fields: Add fields to pull in all the information you want to show in your feed.

Feed Set Up:
- Create a new View of Content of type Episode.
