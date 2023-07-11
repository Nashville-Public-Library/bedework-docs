---
sidebar_position: 7
---

# Example Book List Post

The book list template is good when you want to recommend a lot of titles without writing a full book review.

Write a sentence or two about each book. Write a paragraph overview and display a list without describing each title. Or write an intro paragraph and recommend 30 books using a catalog widget.

In this example, we’re showing off the favorite Newbery Award nominees for 3 different NPL children’s staff members. The content comes from [Lindsay’s Newbery Awards blog post](https://library.nashville.org/blog/2015/01/2015-newbery-awards).

Our post will include the following 3 components:
- Text: Headings and body text
- Catalog Promos: Each recommended book in the body of the post
- Catalog Widget: List of all Newbery winners

## Create a new Blog Entry in Drupal

We’ll start by creating a blog post and adding our main content.
1. Log in to Drupal with your username and password.
1. In the menu bar, select Content > Add Content > Blog Entry.
1. Add a Title. Choose an engaging title that tells the reader what the post is about.
1. Add a Posted Date for your post. This should be the same date you use for scheduling your post.
1. Add Blog Author. Type a first or last name in the author box. Then select the correct name from the list.
1. In the Content tab, use the dropdown menu to add a text block.
   1. Type the heading and text that introduces a catalog promo. We’ve got a short paragraph to introduce the post, then a heading to denote the Top Pick section, then the text that falls between the heading and catalog promo.
1. In the Content tab, use the dropdown menu to add a catalog promo.
   1. Fill out the catalog promo in formation.
1. In the Content tab, use the dropdown menu to add a text block.
   1. Type the heading and text that introduces a catalog promo. Because this is a new section, we should use a Heading 2.
1. In the Content tab, use the dropdown menu to add a catalog promo.
   1. Fill out the catalog promo in form.
1. Save your post. We’ll finish it up in a moment.

## Create a Catalog Widget/Spotlight

1. Go to the library catalog.

1. Create a list. If you already have a list, skip this step.

1. Go to the lists page:
   1. Click the user icon in the upper right.
   ![block image 1](/img/catalog-widget-2.png)
   1. Select “lists” from the menu.
   ![block image 1](/img/catalog-widget-3.png)

1. On the list page, click the Edit button.
![block image 1](/img/catalog-widget-4.png)

1. On the edit screen, mark the list public. Your list must be public to create a catalog spotlight.
![block image 1](/img/catalog-widget-5.png)

1. Once your list is marked public, you have the option to include or exclude the list from search results. Select yes or no, then click Update to save your changes.
![block image 1](/img/catalog-widget-6.png)

1. After saving your changes, you’ll see “create spotlight” at the top of your list. Click “create spotlight.”
![block image 1](/img/catalog-widget-7.png)

1. You’ll be asked to give your spotlight a name. We recommend naming the spotlight the same as your list so the spotlight and list titles match.
![block image 1](/img/catalog-widget-8.png)

1. On the next page, we need to customize the widget. Click Edit.
![block image 1](/img/catalog-widget-9.png)

1. Fill out the following fields:
   1. Name: Give your widget a name.
   ![block image 1](/img/catalog-widget-10.png)

   1. Description: Add a note about where the widget is used. If you’re adding to a blog post, type something like “widget for newbery winners blog post 2015.”
   ![block image 1](/img/catalog-widget-11.png)

   1. Number of Titles: Default is 25, which is generally a good number. You can make this smaller if you like.
   ![block image 1](/img/catalog-widget-12.png)

   1. Uncheck the next three boxes. We do not want to show the title, author, or ratings for titles.
   ![block image 1](/img/catalog-widget-13.png)

   1. Style When Displaying List Widget: Choose Horizontal Carousel.
   ![block image 1](/img/catalog-widget-14.png)

   1. Cover Size to Use: Choose Medium.
   ![block image 1](/img/catalog-widget-15.png)

   1. Custom CSS File: Use https://assets.library.nashville.org/css/aspen-widgets.css
   ![block image 1](/img/catalog-widget-16.png)

   1. Cover Size to Use: Medium
   ![block image 1](/img/catalog-widget-17.png)

   1. For the next two boxes: Uncheck “show list widget title bar.” But DO check “show the view more link.”
   ![block image 1](/img/catalog-widget-18.png)

   1. Display Mode for Search Results: Choose Covers.
   ![block image 1](/img/catalog-widget-19.png)

1. Click Save Changes and Return.
![block image 1](/img/catalog-widget-21.png)

1. Scroll down until you can see the “Collection Spotlight with Resizing” code. Copy ONLY the iFrame URL -- this is the URL in the blue box above the iFrame code. You do NOT need the entire iFrame code snippet. You only need the URL, like the example highlighted below.
![block image 1](/img/catalog-widget-20.png)

## Add Catalog Widget to Blog Post

1. Add the Catalog Widget component to your post.
![block image 1](/img/catalog-widget-23.png)

1. Fill out the form:
![block image 1](/img/catalog-widget-22.png)
   1. Title and iFrame Title: The type title for your widget that will display to the user.
   1. iFrame URL: Paste the iFrame URL from the widget code in catalog.
   1. iFrame Title: Use the same title in both the Title and iFrame Title fields.

1. Review and verify that the widget looks correct. If anything looks weird, check your widget settings.

## Tag Your Post

Every blog post must include at least one tag, though you probably want to use more.

1. Click the Tagging Tab.
1. Click in the Section box. Select at least one top-level section. Top-level section tags do NOT have a dash to the left side of the tag. Tags with the dash are children of the top-level tags. You can choose multiple section tags.

## Add a Thumbnail and Summary

Every blog post must include a thumbnail image and summary.

1. Click the Summary tab.
1. Click Select Image. Then click Add Image to upload your thumbnail image.
1. Type a brief summary of your post in the Summary field. The summary should be a 1-2 sentence overview of what the post covers. You can make words italicized or bold, but please avoid block quotes, links, images, and lists in the summary.

## Schedule Your Post to Publish

Blog posts are not published when you save them. We do this on purpose so you never accidentally publish a blog post. When you’re ready to publish, do NOT use the checkbox unless you want your post to publish immediately.

1. To schedule your post to publish at a certain date and time, use the Scheduling Options box on the right side of the screen. If the box is collapsed, click the title to expand.
1. Type a date and time for your post to publish. This date must match the date in the Posted Date field under the post title.
1. Click Save. Your post will publish within three hours of the time specified.
