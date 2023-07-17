# URL Redirects

A URL Redirect (also called URL forwarding) is a way to give access to a web page from more than one web address. Use a redirect to make a URL shorter (marketing link), to fix a broken link (404), or to make multiple domains point to a single website.

Uses:

- Use for marketing links, alternate links, errors, dead links.
- Use a 301 Redirect to create shortened or alternative URLs that point back to the canonical URL Alias.
- Use a 301 Redirect to redirect dead, moved, consolidated pages (pages we used to have on the site, but they’ve been decommissioned).
- Use a 301 Redirect to redirect a deleted page to a new location. If you delete a published page (if there’s already a URL in the URL Alias field for the page), you must create a URL Redirect for the URL Alias of the page you deleted.

Note: URL redirects do not show up in site search b/c they aren’t pieces of content.

## External Resource and Event Links

Unless a piece of content is a node in Drupal, it cannot come up in search results. Both the **External Resource** content type and the **Event** content type have a way for external content to show up in site search. Both content types can point to a third-party site that needs to be indexed in Drupal, like Interlibrary Loan.

External Resource Content Type (Always Redirects)

- Allows us to create a node for third-party sites, like Wordpress sites, Interlibrary Loan, etc.
- DOES show up in site search.
- Important! The redirect function only works when you’re logged out.

Event Content Type (Only External Events Redirect)

- Allows us to create a node for third-party sites, especially Bedework results.
- DOES show up in site search.
- Important! The redirect function only works when you’re logged out.
