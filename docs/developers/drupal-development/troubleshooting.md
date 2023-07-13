---
sidebar_position: 19
---

# Troubleshooting

## Site is Down

Check Bedework to see if it is up. If Bedework is out, restart. On D7 and early D8, we had an issue where a Bedework outage would bring down all pages that include a Bedework widget. That should not be the case in D9, but check anyway.

## Connection to Pantheon Lost

Troubleshooting terminal Error - No connection to Pantheon. Can occur when trying to communicate with pantheon over MetroWLAN.

1. Turn Wi-Fi on/off, Test connection `git fetch --all` or `ping`
1. Restart computer, test connection
1. If no connection, try again in one hour.
1. If connection is still out - contact ITS. Reference the initial reservation setup in ITS ticket IR442079 (2016)

## Handling Issues with Project-X

Project-X is a wrapper that can work with Lando, Docksal, DrupalVM, etc. Project-X is code to unify and simplify all those environments. Problems are in tooling underneath Project-X. Issues most likely won’t be Project-X specific.

1. Search Google for terms from the error message you get in terminal.
   1. If all the results are all Vagrant related, look for a fix for Vagrant.
   1. If all the results are DrupalVM related, see if something is different in DrupalVM.

1. If you can't find an answer:
   1. Ask Aten for help if you need an answer asap.
   1. Put in a ticket for Project-X on Github if the issue seems bigger than NPL.

## Website Encountered an Unexpected Error

Drupal throws a really generic error message when anything on the site goes wrong: "The website encountered an unexpected error. Please try again later."

There are times this generic error message is shown but it doesn’t always produce a log message, which is frustrating as it’s really hard to troubleshoot. Most of the time if there is no log entry it’s more or less related to a server error.

- Most of the time after you see this error the best thing to do next is navigate to https://dev-npl-d8.pantheonsite.io/admin/reports/dblog.
- On this page you will see all the recent log entries, you should see the fatal error at the top of this page if one has been thrown.

## Local Environment Troubleshooting (Deprecated)

These troubleshooting steps worked when we were using a Docker environment for the NPL D7 site. We’re not using Docker anymore for NPL-D8, but maybe using Lando and Docker for Limitless D7 could cause conflict? No idea really.

1. Vagrant: vagrant up isn’t working
   1. The .vagrant hidden file should never be destroyed. In that file is how vagrant is mapping everything.
      1. If it gets destroyed, go to the Virtual Box UI and delete the environment (npl.test).
      1. Go to terminal and try vagrant up again.
   1. Make sure all Virtual Box is powered off.
      1. Open Virtual Box (application).

1. If things aren’t working well, make sure you don’t have other Docker containers that are listening on other ports.
   1. Find which process is listening on a port: sudo lsof -nP -i4TCP:80 | grep LISTEN  

1. Make sure Lando is off. If you haven’t spun up Lando in a while, you can skip this.
   1. Turn off Lando: lando poweroff

1. Make sure no Docker containers are running. Turn things on and off a few times.
   1. Stop docker containers: docker stop $(docker ps -aq)
   1. See if docker containers are still running: docker ps -a
   1. Remove docker containers by ID (the numbers here represent the number of the container you see after doing docker ps -a): docker rm ff973f88655c 0c297c0dd611
   1. Restart Docker.

1. Make sure apache isn’t running. Our Macbooks have a daemon file that says “start up apache every time my system boots.” So, we may need to stop apache next time we start up again. Need to check on this.
   1. Make sure that apache isn’t running: sudo apachectl stop

1. Turn off devel / twig theme suggestions
   1. Go to npld8: web/sites/development.services.yml
   1. Under twig config, set debug to “false”
