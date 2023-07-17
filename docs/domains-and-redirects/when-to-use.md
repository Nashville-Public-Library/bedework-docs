# When to Use Redirect or Alias or Bit.ly

## We need 2 urls to go to the same content.

- Use a URL Alias for the canonical url (this happens automatically when you create the page).
- Use a URL Redirect to create the second url (the redirect will point to the alias - the canonical url).

## Need to create a marketing-friendly URL.

- Use a URL redirect to create marketing-friendly URLs like library.nashville.org/summerchallenge or library.nashville.org/nashvillereads.

## Need a link to a third-party-site (ILLiad or Wordpress) and need a marketing link.

- When we link to a third-party site, we want that site to come up in site search. Create a node using the External Resource Content Type. This allows the third-party site to show up in site search.
- Create a shorter link using a URL Redirect that points to the External Resource node.

## Need a marketing URL that points to an Event Series in Bedework

- Because this is an event series, you'll create a node using the Event Content Type. You'll set the node to "external" and only add the Bedework URL and fill out required fields.
- For the marketing link, create a URL Redirect that points to the Event node.

## Need to use EZ Proxy Links on the Database Nodes.

- For database nodes, the code manually overrides the link display, bypassing the Drupal sanitization. We are displaying what is stored in the database, which looks like it saves exactly what is in the field when editing the node.

## Need to use EZ Proxy Links on the Main Menu

- Point the menu link to the database node. User will have an extra click to get to the database.

## Need to use EZ Proxy Links on Home Promos that point to a database.

- Do not point directly to the database. Point to the database node on the NPL site.

## Need to add Bedework Links to the Menu or Home Promos.

- Use a bit.ly link.
