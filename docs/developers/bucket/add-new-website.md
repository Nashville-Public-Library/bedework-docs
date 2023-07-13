---
sidebar_position: 3
---

# Adding a New website to Bucket

## Get New DNS Entry

1. Email ITS and ask them to create a DNS entry for the site you want to make:
```
Please create internal and external DNS A records for [sitename].library.nashville.org and point it to this IP: [get bucket IP from password manager].
```

1. When ITS completes the DNS entry work, test on terminal:
   1. Type: dig [subdomain].library.nashville.org
   1. This should return the bucket IP if it is set up correctly.  

## Create Site Folder and Index File

1. Create a new folder for the site:
   1. In terminal, log in to the server.
   1. Go to data/www/: `cd data/www/`
   1. Create a new folder: `mkdir [sitename]`

1. Update permissions on the new folder: `sudo chown apache:apache [folder-name]`

1. Inside the new [sitename] folder, create a file called index.html.

## Create a Stanza for the HTTP Version of the Site

1. Go to /etc/httpd/conf: `cd etc/httpd/conf`

1. Edit the httpd.conf file: `sudo nano httpd.conf`

1. Update the stanza to add the new site.

1. Restart apache: `systemctl restart httpd`

1. Make sure apache is running: `systemctl status httpd.service`

1. Test on the web to see if you can get to the new site's index.html page.

1. Make sure that the Virtual Host settings here match what is in the ssl.conf file.

## Create a Stanza for the HTTPS Version of the Site

1. Go into /etc/httpd/conf.d: `cd etc/httpd/conf.d`

1. Edit the conf file with nano: `sudo nano ssl.conf`

1. Jump to the bottom of the file where the virtual hosts stanzas are.

1. Add a new `<VirtualHost>` stanza by copying an existing setup and pasting below.
   1. Put your cursor where you want to start highlighting.
   1. Type this key combination to set the starting mark: Ctrl + Shift + 6
   1. Use the down arrow (or up arrow) to start highlighting.
   1. Cut the highlighted text (because we cannot find a command for copy): CTRL + K
   1. Paste once: CTRL + U
   1. Paste again: CTRL + U
   1. Edit the second pasted copy so it uses the new [sitename].
   1. Save

1. Restart apache: `systemctl restart httpd`

1. Make sure apache is running: `systemctl status httpd.service`

1. Test on the web to see if you can get to the new site's index.html page.

1. Make sure that the Virtual Host settings here match what is in the httpd.conf file.
