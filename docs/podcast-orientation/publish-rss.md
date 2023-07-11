---
sidebar_position: 4
---

# Publish / Refresh XML Feed

## Add Podcast Name to Taxonomy in Drupal

Make sure that the new podcast has been added to the Podcast Series taxonomy. Creating the taxonomy term is how we generate the XML feed.

1. Add the new podcast term.
1. Get the XML feed address by placing the term ID in the URL: `https://library.nashville.org/podcasts/`[term-id]`/feed.xml`
1. Edit the podcast term to paste the XML feed address in the RSS subscription field.

## Publish New Podcast Feed

### Apple podcasts

Note: Login in Lastpass (need to be in Shared Systems folder)

1. Go to https://itunesconnect.apple.com/login
1. Login using username and password (currently this is Kyle Cook’s login and we need to figure out a way to change this).
1. Click Podcasts Connect.
1. Paste in the XML feed URL.
1. Click “validate” button.
1. Check the info and click “submit” button.
   1. Apple will send an email to the podcast email address when the podcast is accepted. This email address is our LibAnswers email.
   1. You can also refresh the podcasts admin page to see when it is updated.
1. Once the podcast is verified, search for the podcast on Apple Podcasts and copy the URL.
1. Paste the podcast URL into the “apple podcasts” section of the term page.
1. Save the term page.

### Google Podcasts

Note: Login in Lastpass (need to be in Shared Systems folder)

1. Go to https://podcastsmanager.google.com/
1. Login to the nplwebservices@gmail.com account. Login using username and password saved in Lastpass.
1. Find the menu and click “add show.”
1. Paste in the XML feed and click next.
1. Click to send verification code. Code will be sent to nplwebservices@gmail.com account. Or it may be sent to LibAnswers.
1. Paste verification code into Google Podcasts.
1. Google will review the feed, which may take a few days. Google FAQs say: “If this is a new show in Podcasts Manager, wait a few days for Google to start serving your podcast and accumulating data.” So check back a few days after submitting the podcast.
1. You might need to generate a link directly to the podcast (feed must be served first): https://search.google.com/devtools/podcast/preview
1. Paste the podcast URL into the “google podcasts” section of the term page.
1. Save the term page.

### Pocket Casts

Note: No login info needed

1. Go to https://www.pocketcasts.com/submit/
1. Enter the podcast XML feed URL.
1. Mark the feed “public.”
1. Click Submit.
1. You should see a “success” message and a Pocket Casts URL. Copy the URL and paste into the podcast term “feeds” section.
1. Save the term page.

### RSS

Note: No login info needed

1. Get ID for the podcast term.
1. Copy this URL: https://library.nashville.org/podcasts/[term-id]/feed.xml
1. Paste into the podcast term “rss” section.
1. Replace the term-id text with the actual ID for the podcast term.
1. Save the term page.

### Spotify

Note: Login in Lastpass (need to be in Shared Systems folder)

1. Go to https://podcasters.spotify.com/
1. Login using username and password saved in Lastpass.
1. Click the menu.
1. Click “add or claim your podcast.”
1. Click “get started.”
1. Paste in the XML feed -- you should get a “next” button.
1. Click “send code” -- Spotify will send a code to the email address associated with NPL’s Spotify account. This is currently connected to LibAnswers.
1. Log in to LibAnswers and get the code.
1. Type the code in the field in Spotify.
1. Click “next.”
1. Fill out the form for language, host, category, etc.
1. Click submit. You should get a success screen with a URL for your podcast on Spotify. Copy the link.
1. Paste into the podcast term “spotify” section.
1. Save the term page.

### Stitcher

Note: Login in Lastpass (need to be in Shared Systems folder)

1. Go to https://partners.stitcher.com/
1. Login using username and password saved in Lastpass.
1. Click “add a show.”
1. Paste in the XML feed for the podcast.
1. Click Next.
1. Stitcher will ask you to verify the email address associated with NPL’s * Stitcher account. This is currently connected to LibAnswers: ask@nashvillepubliclibrary.org. It may take several days for Stitcher to send a verification email.
1. Go to the podcast in Stitcher and click “manage show.”
1. Paste in the show URL. This is the URL of the podcast series.
1. Go to the podcast in Stitcher admin and click “promote show” and copy the Stitcher URL.
1. Paste Stitcher URL into the podcast term “stitcher” section.
1. Save the term page.

### TuneIn

Note: No login info needed

1. Go to https://cms.tunein.com/podcasters/
1. Scroll down and find the “Publish a Podcast” button -- click the button.
1. Fill out the form.
1. Click submit.
1. You’ll get an email when the podcast has been added to TuneIn. After you get the email, search TuneIn to find the podcast URL.
1. Paste the TuneIn URL into the podcast term “tunein” section.
1. Save the term page.

### YouTube

We aren't currently putting podcasts on YouTube, but we can if we get a video file.

## Refresh Existing Podcast feeds

See information above and look for a “refresh feed” link or something similar.
