---
sidebar_position: 9
---

# Install, Update, Uninstall Modules

## Install a Module or Themes

1. Find a module on drupal.org.

1. In terminal, use Composer to install the module:  
`composer install drupal/[module-name]`

1. Enable the module using Drush (below is a Project-X Drush command):  
`px drupal en [module-name]`

1. Test the module.
   1. If it works, commit your work.
   1. If it doesn't work, follow instructions below for uninstalling and removing modules.

## Uninstall a Modules or Themes

Uninstall modules from Drupal before using composer to remove modules from the project.

1. Disable the module:  
`px drupal pm:uninstall [module-name]`
1. Remove the module with composer:  
`composer remove drupal/[module-name]`
1. Commit your work.

## Patch a Contributed Module

See Aten video (Travis) video for demonstration:
- File on Z drive: *Aten Training_2019-08-06_Podcast-field-mapping-and-applying-a-PATCH*
- Demo starts around the 12:00 minute mark.

Step-by-Step from Video:  

1. Go to the module's page on [drupal.org](https://drupal.org) and look at reported issues.
1. Select an issue and view the patch by clicking on the .patch file at the top of the individual issue page.
1. Update the module with the patch.
   1. For an easy patch, we can update the contributed module itself.
      1. Open the .module file for the contrib module: web > modules > contrib > [module-name]
      1. Go to the specific file defined in the patch.
      1. Add everything with a plus sign (+). Remove everything with a minus sign (-).
      1. Test on local machine and see if it works. You shouldn’t have to clear the cache.
   1. If it's a huge patch, don’t add it manually.
1. Open the composer.json file. At the bottom of the file, there should be a spot for patches in “patches:” section.
   1. Add the issue and a link to the patch to the composer.json file.
   1. Save the composer.json file.
1. Go to terminal and run the composer install command to apply the patch:  
`composer install`

## Update Modules / Drupal Core / PHP

### Background

- Update.php is for when modules to make changes to your database.
- When you update modules, you're changing the local database, so the database on dev test and live will need to get updated config changes. This happens automatically with Pantheon (it’s why you check the “update.php” box when deploying).
- You can add /update.php to the end of the site URL to force the database to update.

### Update a Module

1. Create a feature branch for your module update(s).  
`git flow feature start NPLD8-xxx`
1. View available updates on your local: /admin/reports/updates
1. Update module:  
`composer update drupal/[module_name]`
1. Update database. This goes through all the updates, looks at any schema changes happening in the database, and lets you know what they all are.  
`px drupal updb`
1. Type yes to run the updates.  
`yes`
1. Check the site to make sure it is working. Test anything mentioned in the update notes.
1. If all is good, commit your work.

### Troubleshooting a Module Update

If the module isn’t working, roll back the change by doing the following:

1. If the module didn’t have database updates:
   1. Checkout changes to the lock file:  
   `git checkout -- composer.lock`
   1. Update the lock file:  
   `composer update --lock`
   1. Check the available updates report on your local environment to make sure the module update got rolled back: /admin/reports/updates
1. If the module did have database updates:
   1. Get the database from live:  
   `px pantheon:sync`
   1. Do composer install:  
   `composer install`
1. View changes:  
`git diff [file name, probably composer.lock]`
1. Export config:  
`px drupal cex`
1. Commit changes.
