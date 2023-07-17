# News Landing Page on Drupal 7

/press-room
/press-room/media-hits
/press-room/press-releases
/news-types/media-hit
/news-types/press-release

News Types Taxonomy

1. Create taxonomy on live site. The vocabulary and terms should be created on Live because vocabularies and terms are content.
1. Once vocabulary and terms are created, pull the database down to Test, Dev, and Local.

Press Room Content Type - Create the content type on Local so it can be exported as code.

- Title
- News Item Type (term reference for News Type taxonomy) - field_news_item_type
- Date - field_date
- Media Hit Source Link (URL for the online article) - field_media_hit_source
- Media Hit Source Name (title for the online article) - field_media_hit_source_name
- Press Release File (uploading PDFs) - field_press_release_file

Press Room Views - Create the views on Local so they can be exported as code.

- Media Hits page and block - display fields
- Press Releases page and block - display fields

Press Room Context - Create context on Local so it can be exported as code.

- Name = news (lowercase)
- Tag = Page
- Path = press-room
- Views = add media hits and press releases
