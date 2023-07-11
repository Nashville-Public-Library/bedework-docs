---
sidebar_position: 2
---
# Locations Landing Page

The locations landing page is a Basic Page with a text component and a view block. The view block shows all branches. Main is at the top because of a checkbox on the branch content type that gives Main priority.

The Google Map is widget code in a text box set to Full HTML Raw.

## Google Maps Widget

### Edit / Update

1. Log in to Drupal site
1. Go to the locations page.
1. Click Edit.
1. Click Edit for the text component.
1. You should see the embed code in the source view. Update the source code.

### Making the Google Map

This is what Aten originally had in the text box:
```
<div style="overflow:hidden;height:500px;">
<div id="gmap_canvas" style="height:500px;">&nbsp;</div>
<style type="text/css">
#gmap_canvas img{max-width:none!important;background:none!important}
</style>
<a class="google-map-code" href="http://www.map-embed.com" id="get-map-data">www.map-embed.com</a>
</div>
```

For the current map, Kyle used Google My Maps and used the Share tools and selected “Embed on my site” option.

## Closure Notices

When an individual location has content in the "Extended Closure" field, the hours block on the landing page is replaced with the message in the "Extended Closure" field.
