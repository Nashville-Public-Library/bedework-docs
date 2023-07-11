---
sidebar_position: 5
---

# Domain Redirects

## Redirect a Domain to a Wordpress Site

1. Purchase the domain through ITS. If it must be purchased by auction, buy and then transfer to ITS. If a domain is already owned, but not managed by Metro ITS, transfer the domain to Metro.

1. Once the domain purchase is final, go to cpanel (see passwords for login info) and PARK the new domain.

1. Set up a redirect from the new domain to the site on nashvillepubliclibrary.org:
   1. You should be able to set up a redirection from the Parked Domains list by clicking Manage Redirection:
   1. If that option is not available or if you are at the cpanel home menu, do this instead:
      1. Click Domains from the list
      1. Click Redirects from the list
      1. Choose the domain we’re redirecting (it will be the one you purchased). Type in the URL of the nashvillepubliclibrary.org site you want the new domain to point to.

1. Email ITS and let them know you have redirected X domain to a new URL. Give ITS the host gator server IP (saved in passwords).

```
Hi Help Desk,

A few months ago, you guys purchased two domains for the library:
studionpl.com
studionpl.org

Both URLs need to redirect to this IP address: xxx.xxx.xxx.xxx (the
  IP address for  http://nashvillepubliclibrary.org).

Once that's complete, I'll get in touch with the host to complete
the redirect to the correct spot on nashvillepubliclibrary.org.

Can you help?

Thanks,
```

## Redirect a Domain to a Drupal Page

Route an owned domain name (like studionpl.org) to an internal page on the library’s Drupal site.
- Currently: ITS forwards the domain to the internal page (for example, https://library.nashville.org/studionpl) via Hover.
- Need to Test: Hover cannot forward https domains, but Drupal has a way to forward domains to a page using a few lines of code in settings.php. That code routes traffic from the domain name to a specific page on the Drupal site. Need to test this.

1. Purchase the domain through ITS. If it must be purchased by auction, buy and then transfer to ITS. If a domain is already owned, but not managed by Metro ITS, transfer the domain to Metro.

1. Make the change in Drupal settings.php file. We figured out how to do this from Pantheon Documentation. Cannot test on multidev (I dont' think) so push to production to verify the redirect works.

1. Point the domain name(s) to Drupal.
   1. Get the right URL from Pantheon.
      1. For NPL site: Forward the domain to the live URL on our web host. This is the easiest option and what we recommend.
      1. For LL site: Use the platform domain for the LL site.

1. Send ITS with a DNS service request with the associated domains and the IP address you want them sent to.

```
Hi Help Desk,

Nashville Public Library owns the following domain name(s):
[domain name]

We need to forward traffic from the above domain name(s)
to library.nashville.org/[url-path].

Can you please set up this domain the same as studionpl.com and
nashvilletalkinglibrary.com? When we did this last, we forwarded the
domain to the internal page via Hover.

If the DNS change is successful, a user typing [domain name] will be
redirected to library.nashville.org/[url-path].

Can you help?

Thanks,
```

1. Test to verify that the redirect works.
   1. If you run into trouble, double check that there aren’t any redirects in Drupal that need to be deleted or changed.
   1. If this was a domain name we used with Wordpress, log in to Hostgator and make sure the domain isn’t parked / redirected.
   1. If there aren’t conflicting redirects in Drupal, report issues to ITS.
