---
sidebar_position: 4
---

# Refresh Database on Local

You do not need to refresh the database as often as you pull code. Refresh the database under the following conditions:
- It's been a while and you want the newest content on your local.
- You've added content to the live site that you need on local in order to complete work on a feature.

## Get the Live Database

1. In terminal, make sure you’re in the project folder:  
`cd ~/Sites/npl-d8`
1. In terminal, type:  
`px pantheon:sync`
1. Choose which database you want:  
`live`
1. The local database will get updated with the most up-to-date content.

## Enable Stage File Proxy

When you get the live database, the Stage File Proxy module will be disabled. If you want to see images, you'll need to re-enable it.

1. In terminal run the Drush enable command:  
`px druapl en [module-name]`
1. Clear cache:  
`px drupal cr`
1. You're done. Do NOT commit the module.
