---
id: promotion
sidebar_position: 4
---

# Promos and Promotion Component

Promo blocks and the promotion component work together to form rows of promo content. Designed for use on the homepage, but can be used anywhere that you plan to use promo blocks.

![block image 1](/img/promotion-0.png)

## Add a Promotion Layout Component

The promotion component is a layout tool that organizes promo blocks in 3-column rows. If you're using promo blocks, the promotion component must be added to the page first, then you can add promos inside this component. If you're page already has this component, skip to the other sections to learn how to add or swap out promos.

1. Add a promotion component to your page.
![block image 1](/img/promotion-1.png)

1. In the columns dropdown menu, select 3. This will give you 3 columns, or 3 promotions across the page.
![block image 1](/img/promotion-2.png)

1. Select an option for adding a block: make a new block or add an existing block. Note: See the info for the promo block for step-by-step help on creating promo blocks.
![block image 1](/img/promotion-3.png)

1. Add promo blocks. See details on adding blocks in the next section, below.

## Promo Guidelines

- Link to Bedework: Use bit.ly to create links for individual events in the Bedework Events Calendar. Bedework links do not work natively in Drupal.
- Link to Databases: Use the link to the database landing page on Drupal, not the database. Some database links do not work natively in Drupal.
- Images: Avoid call to action or title text in your image. If you do use text, use it sparingly. Text as image, like the VOTE graphic, is fine b/c text is part of the artwork.
- Translation: Always make a promo in English first, even if we’re making it for the Spanish or Arabic landing page.

## Promo Image Dimensions

- Width: 600px
- Height: 402px

## Add a New Promo Block (Inline Entity Form)

1. Prep your image

1. Go to Content > Filter for “homepage” > Once you find the Homepage, click **Edit**.

1. Select the Promotion row you want to update by clicking the **Edit** button.
![home page components](/img/site-orientation-4.png)

1. Click **Add New Custom Block** (that’s the inline entity form).
![home page components](/img/site-orientation-5.png)

1. Fill out the form:
   1. Block Description: Type the Block Description. This will NOT be seen by the user. This is for a staff-facing description to help you find reusable promos later on.
   1. Home Promo Title: Yellow title text on the home promo.
   1. Home Promo Body: Gray text that displays under the Home Promo Title.
   1. Mega Menu Body: Text serves as both title and description in the mega menu. You may want to adjust the wording for the mega menu display.
   1. Link: Add a link where the promo will take users. Can be an internal link or external.
   1. Image: Select the image for the promo. You must add alt text. The same image will be used for both the Home Promo and Mega Menu Promo displays.

1. Click **Create Custom Block**.
   1. Note: The new promo is not saved until you save the homepage.
   1. Also note: We have some tidying to do before we can save the page.

1. Our row should now have 4 promo blocks. But, this row is only allowed to have 3 promo blocks. Click **Remove** next to one of the other promo blocks to get back to 3 for this row.
![home page components](/img/site-orientation-6.png)

1. You’ll get a prompt to double check if you want the block removed. If you might use the block again in the future, just click **remove**. If you will never use the promo again and want to delete it from the block library, check the box next to **delete this custom block from the system.**
![home page components](/img/site-orientation-7.png)

1. You should be back down to 3 blocks. On the right side of the screen, add a revision message to document the changes.

1. Save.

1. Immediately go to the homepage, [(https://library.nashville.org](https://library.nashville.org) and make sure everything looks okay.

1. If not, edit the page and fix any errors.

## Add an Existing Promo Block (Swap Promos)

1. Go to **Content** > Filter for **homepage** > Once you find the Homepage, click **Edit**.

1. Select the Promotion row you want to update by clicking the **Edit** button.
![home page components](/img/site-orientation-4.png)

1. Click **Add Existing Custom Block**.
![home page components](/img/site-orientation-8.png)

1. Click **Select Promotions**.
![home page components](/img/site-orientation-9.png)

1. Check the box next to the promo block you want to add, then click the **select content** button. Use Title and Description at the top of the form to limit your list of promos.
![home page components](/img/site-orientation-10.png)

1. Our row should now have 4 promo blocks. Click **Remove** next to one of the other promo blocks to get back to 3 for this row.  

1. You’ll get a prompt to ask if you want to remove the block. Click **remove.**

1. You should be back down to 3 blocks. On the right side of the screen, add a revision message to document the changes.

1. Save.

1. Immediately go to the [homepage](https://library.nashville.org) and make sure everything looks okay.

1. If not, edit the page and fix any errors.

## Bulk Add Promos for Later use
You can add notifications to use later. Instead of going to the home page and adding a new block to the page, you’ll go to the block creation section in Structure > Block Layout and add blocks for use later.

1. Log in to the web site at [https://library.nashville.org/user](https://library.nashville.org/user) with your username and password.

1. In the menu bar, select **Structure** > **Block Layout** > **Add custom block**.

1. Select **Promo** from the list of options.

1. Create the promo according to instructions found in the Promo Component instructions.

1. Saving a promo created this way publishes the block, but the public cannot see it unless it has been placed on the homepage. You must place the block on the homepage (as outlined above) to publish the block to the homepage.

## Translate Promo to Spanish or Arabic (Coming Soon)

1. Log in to Drupal

1. Select **Find Content**

1. Find your **Promo** in the list of content. Click the **edit** link for the promo.

1. Promos that are ready for translation will have a **Translate** tab next to the View and Edit tabs.
   1. If you see the Translate tab, you’re ready to create a translation.
   1. If you do not see the Translate tab, look at the language drop down. If it says “Language Neutral,” change the setting to “English.” Then, save the promo. Always start promos in English. Never create a Spanish or Arabic promo without an English version first.

1. Click the **Translate** tab.

1. Click “add” next to Spanish or Arabic.

1. Update text and image: Paste the translated title into the Promo field. Paste the translated text into the Text field. You can also swap out images if you want the translated node to have a different image than the English node.

1. Leave the URL alone. Be sure the URL does NOT have a language code in the URL field.

1. Save

1. On the promo page, in view mode, test the URL to make sure it goes to the right place.

1. Repeat steps to add translations in additional languages.
