# Redirect a Domain to Wordpress, Drupal, Bucket

## Drupal

Route an owned domain name (like studionpl.org) to an internal page on the library’s Drupal site. ITS forwards the domain to the internal page (for example, https://library.nashville.org/studionpl) via Hover.

1. Email ITS to ask them to purchase the domain name(s).
      1. If a domain name must be purchased by auction, buy it and then transfer to ITS.
      1. If a domain is already owned, but not managed by Metro ITS, transfer the domain to Metro.
1. After the domain purchase is complete, email ITS with a DNS service request with the associated domains and the IP address you want them sent to. Example email:  
```
Hi Help Desk,

Nashville Public Library owns the following domain name(s):
[domain name]

We need to forward traffic from the above domain name(s) to library.nashville.org/[url-path].

Can you please set up this domain the same as studionpl.com and nashvilletalkinglibrary.com? When we did this last, we forwarded the domain to the internal page via Hover.

If the DNS change is successful, a user typing [domain name] will be redirected to library.nashville.org/[url-path].

Can you help?
```
1. Test to verify that the redirect works.
      1. If you run into trouble, double check that there aren’t any redirects in Drupal that need to be deleted or changed.
      1. If this was a domain name we used with Wordpress, log in to Hostgator and make sure the domain isn’t parked / redirected.
      1. If there aren’t conflicting redirects in Drupal, report issues to ITS.

## Bucket

1. Email ITS to ask them to purchase the domain name(s).
      1. If a domain name must be purchased by auction, buy it and then transfer to ITS.
      1. If a domain is already owned, but not managed by Metro ITS, transfer the domain to Metro.
1. After the domain purchase is complete, email ITS with a DNS service request with the associated domains and the IP address you want them sent to. Example email:  
```
Hi Help Desk,

Nashville Public Library owns the following domain name(s):
[domain name]

We need to forward traffic from the above domain name(s) to [sub-domain].library.nashville.org.

Can you please set up a redirect through the registrar (Hover)? When we did this last, we forwarded the domain to the internal page via Hover.

If the DNS change is successful, a user typing [domain name] will be redirected to [sub-domain].library.nashville.org.

Can you help?
```
1. Test to verify that the redirect works.
      1. If you run into trouble, double check that there aren’t any redirects in Drupal that need to be deleted or changed.
      1. If this was a domain name we used with Wordpress, log in to Hostgator and make sure the domain isn’t parked / redirected.
      1. If there aren’t conflicting redirects in Drupal, report issues to ITS.

## Wordpress

1. Email ITS to ask them to purchase the domain name(s).
      1. If a domain name must be purchased by auction, buy it and then transfer to ITS.
      1. If a domain is already owned, but not managed by Metro ITS, transfer the domain to Metro.
1. Once the domain purchase is final, go to cpanel (see passwords for login info) and PARK the new domain.
1. Set up a redirect from the new domain to the site on nashvillepubliclibrary.org:
      1. You should be able to set up a redirection from the Parked Domains list by clicking Manage Redirection.
      1. If that option is not available or if you are at the cpanel home menu, do this instead:
         1. Click Domains from the list
         1. Click Redirects from the list
         1. Choose the domain we’re redirecting (it will be the one you purchased). Type in the URL of the nashvillepubliclibrary.org site you want the new domain to point to.
1. Email ITS and let them know you have redirected X domain to a new URL. Give ITS the host gator server IP (find the IP in password manager). Exmaple email:   
```
Hi Help Desk,

A few months ago, you purchased x domains for the library:
[domain]
[domain]

Please point the URL(s) to this IP address: xxx.xxx.xxx.xxx (the IP address for  http://nashvillepubliclibrary.org).

Once that's complete, I'll get in touch with the host to complete the redirect to the correct spot on nashvillepubliclibrary.org.

Can you help?
```
1. Verify that the domain name is going to the right Wordpress site.
