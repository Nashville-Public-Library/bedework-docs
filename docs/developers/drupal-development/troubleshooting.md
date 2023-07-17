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

Project-X is a wrapper that can work with Lando, Docksal, DDEV, etc. Project-X is code to unify and simplify all those environments. Problems are in tooling underneath Project-X. Issues most likely won’t be Project-X specific.

1. Check the version of Project-X. See if we're up to date.

1. Search Google for terms from the error message you get in terminal. If all the results are DDEV related, look for a fix for Vagrant.

1. If you can't find an answer, put in a ticket for Project-X on Github if the issue seems bigger than NPL.

## Website Encountered an Unexpected Error

Drupal throws a really generic error message when anything on the site goes wrong: "The website encountered an unexpected error. Please try again later."

There are times this generic error message is shown but it doesn’t always produce a log message, which is frustrating as it’s really hard to troubleshoot. Most of the time if there is no log entry it’s more or less related to a server error.

- Most of the time after you see this error the best thing to do next is navigate to https://dev-npl-d8.pantheonsite.io/admin/reports/dblog.
- On this page you will see all the recent log entries, you should see the fatal error at the top of this page if one has been thrown.

## Local Environment Troubleshooting (Deprecated)

These troubleshooting steps worked when we were using VirtualBox, but we're using DDEV now.
