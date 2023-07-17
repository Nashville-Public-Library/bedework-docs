# Overview

## Sites on Bucket

Directories in data/www/:

- [Assets](https://assets.library.nashville.org): Hosts css files, javascript files, startpages, finding aids, and media.
- [Firesign](https://firesign.library.nashville.org): Digital signs.
- [Salon](https://salon.library.nashville.org): Salon static site.

## Relevant Config Files on Bucket

/etc/httpd/conf/httpd.conf

- List of virtual hosts.
- Port 80 is the non-https port. If anyone goes there, it redirects users to the https port.

/etc/httpd/conf.d/ssl.conf

- This is the part that really matters. Port 443 takes users to the https file.
- List of virtual hosts for each sub-site.
- Each site has its own specific document root.
