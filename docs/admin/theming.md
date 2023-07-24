---
sidebar_position: 6
---

# Theme

## Language settings / wording

To change wording / labels / longer text, go to: `.../wwwDocRoot/3.10/calrsrc.MainCampus/default/strings.xsl`

Examples of what the strings file solves:
-	Find the correct place to change the text for “today” and “upcoming” (or “reset date” and “grid view”)
-	Find the correct place to change the text ONGOING to EXHIBITS

About the Bedework 3.10 theme files (where stuff lives)
Share and Download icons for each event live in three places (I think, based on Bedework Vendor’s feedback):
-	widgetEventList.xsl
-	events.xsl
-	eventListRange.xsl

## Change the Featured Images
1.	Open Cyberduck
1.	Double click on Bedework.
1.	If an “unknown host key” or “unknown fingerprint” message appears, click Allow.
1.	The file to update is `/opt/bedework/3.12/quickstart-latestVersion/bw-calendar-xsl/content/calrsrc.MainCampus/themes/nashville/featuredEvents.xsl`.
1.	Once updated, you need to type this in the browser to activate it:  [https://events.library.nashville.org/cal/main/showEventList.rdo?refreshXslt=yes](https://events.library.nashville.org/cal/main/showEventList.rdo?refreshXslt=yes)
