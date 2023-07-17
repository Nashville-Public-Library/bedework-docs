# WordPress Redirects

## 301 Redirect Using cPanel

1. Log in to WordPress host and go to cPanel.
1. Find “Domains” and click “Redirects”.
1. Add a new redirect.
1. Fill out the form. Use permanent (301) for the redirect.
1. Save.
1. Test.

## 301 Redirect Using the .htaccess File

[See Source for the .htaccess Info Below](https://wpastra.com/redirects-in-wordpress/)

### About the .htaccess File

- .htaccess is a configuration file used to change how a web server handles various requests.
- The .htaccess file is located in the root folder or central directory of your WordPress website.
- Turn on the option to “show hidden files” in your FTP Client or File Manager and you should now see the .htaccess file.
- Make sure to backup the .htaccess file before making any changes to it.
- .htaccess is written in Apache language.

### Redirecting Single Posts/Pages

Paste the following code in your .htaccess file and replace the URLs with your own. Notice that for the old URL we only used the slug (some-old-URL), while for the new one we used the entire URL (https://yoursite.com/some-new-URL). Pro Tip: Be sure to check that the new URL has the correct protocol (http/https).

Redirect 301 /some-old-URL https://yoursite.com/some-new-URL

### Redirecting an Entire Website

Paste the following code in your .htaccess file and replace the olddomain and newdomain values with your actual domains. Pro Tip: Be sure to also check that the new values bear the correct domain extensions i.e. .com, .org, .net, etc.

```
<IfModule mod_rewrite.c>
  RewriteEngine On
  RewriteCond %{HTTP_HOST} ^olddomain\.com$ [OR]
  RewriteCond %{HTTP_HOST} ^www\.olddomain\.com$
  RewriteRule (.*)$ http://www.newdomain.com/$1 [R=301,L]
</IfModule>
```

When deleting an entire WordPress Network site, we could use wildcards to redirect every URL on the old site to its new destination. Update the highlighted portion to use the wildcard search we used in the Redirection module: ​/wilsonbookarts​/+.*

```
<IfModule mod_rewrite.c>
  RewriteCond %{HTTP_HOST} ^www.mydomain.com$
  RewriteRule (.*) http://mydomain.com/$1 [R=301,L]
</IfModule>
```
