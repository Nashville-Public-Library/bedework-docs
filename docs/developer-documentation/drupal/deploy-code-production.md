---
sidebar_position: 8
---

# Deploy to Production

Follow this process once a feature is approved and we're ready to deploy to production.

## Merge Feature into Develop

When a feature branch is approved, merge it into develop branch so everyone can pull from the most up to date codebase.

1. Go to the npl-d8 project in Github: [NPLD-8](https://github.com/Nashville-Public-Library/npl-d8)
1. Verify the pull request is ready to merge (merge pull request button should be green).
1. Click the “Merge Pull Request” button.
1. In the box above the “Confirm Merge” button, type the ticket IDs covered with this merge.
1. Click the “Confirm Merge” button.
1. Delete the branch in Github.

## Merge Develop into Master

When you are ready to deploy changes to Pantheon, merge develop into master using either the Github GUI or Terminal, then push to Pantheon.

### Use Terminal (recommended)

1. Go to develop branch:  
`git checkout develop`
1. Pull to get most up to date develop code:  
`git pull origin develop`
1. Checkout master:  
`git checkout master`
1. Pull to get most up to date master code:  
`git pull origin master`
1. Merge develop into master:  
`git merge develop`
1. If you end up in VIM, do esc, colon, write, quit:  
esc button then `:wq`
1. Push to Pantheon:  
`git push origin master`
1. Go to [CircleCI](https://circleci.com/), to see the build process run. The build process deploys master to Pantheon dev.  

### Use the Github GUI (alternate option)

1. Go to the npl-d8 project in Github: [NPLD-8](https://github.com/Nashville-Public-Library/npl-d8)
1. Click the Pull Requests tab.
1. Click the New Pull Request button.
1. For “comparing changes” options:
   1. Base = master
   1. Compare = develop
1. Review the commits that are going into this pull request just to be sure it is what you expected.
1. Click the “Create Pull Request” button.
1. Type the release number in the title: *Build x.x.xx*
   1. Check Pantheon dev to see what release number we’re on.
   1. Minor release numbers go to 20 then you start a new major release.
1. Click the “Create Pull Request” button.
1. Click the “Merge Pull Request” button.
1. Go to [CircleCI](https://circleci.com/), to see the build process run. The build process deploys master to Pantheon dev.

## Review on Pantheon

Once code is on Pantheon, test on dev and test sites before deploying to live.

### Make a Backup of Live

1. Log in to Pantheon: [Pantheon](https://pantheon.io)
1. Click the Live tab.
1. Click the Backups option from the left menu.
1. Start a backup. A backup is a good idea before a deploy to live. Start the backup now b/c it may take a while.

### Review on Dev

1. Log in to Pantheon: [Pantheon](https://pantheon.io)
1. Click the Dev tab.
1. Click the link to visit the dev site.
1. Verify that the changes from the feature branch are all present and functioning correctly.
1. If all looks good, click on the Test tab.

### Deploy from Dev to Test

1. On the Test tab, write a deploy message. Include the build number, like this: "Deploy build x.x.x: Updates to X Y Z."
1. Make sure all the checkboxes for the deploy are checked: run update.php, clear caches, pull files and database from live.
1. Click the “deploy code from dev to test” button.
1. Click the link to visit the test site.
1. Verify that the changes are all present and behaving correctly.
   1. As you are testing, write down any deploy steps you need to repeat on live.
   1. If all looks good, click on the Live tab.

### Deploy from Test to Live

1. If all changes look good on test, click the live tab.
1. Verify that your backup is finished.
1. Click the “deploy code from test to live” button.
1. Visit the live site.
1. Verify the site is up.
1. Verify that the changes are all present and behaving correctly.
1. If all looks good, you’re done! If all is NOT good, see “troubleshooting” steps below.

## Troubleshooting

### Issues Merging Feature into Develop

Note, if you run into trouble during the merge, you might have issues with the composer.lock file and the hash in the file. You may not be able to use the Github interface completely because sometimes you have to run “composer update --lock” if there are merge conflicts with composer.

### Issues Merging Develop into Master

Master branch shouldn’t have a build failure, but it is possible.

If the build process fails when you’re on the master branch:
1. Go to Terminal.
1. Do pull:  
`git pull origin master`
1. Do config import: px drupal cim
1. Update the lock file: composer update --lock
1. Make sure hash files are not conflicting.
1. Fix anything on master that is weird, fix it on master, commit changes, and then push to master.

If you make changes on master, you have to put all changes in develop once everything is fixed:
1. cd into develop
1. remerge changes from master into develop: git merge master
1. Push changes to develop: git push origin develop
1. Deploy Changes on Pantheon

### Config Will Not Import on Pantheon Dev

When pushing from local to Pantheon Dev, you might run into a scenario where config won't import. This often happens when there are core updates and lines of code are moved around, but not really changed.

1. Import config.
   1. Try importing config via terminus.  
   `px pantheon:drupal cim`
   1. Try importing config via the UI.
1. If config changes aren't imported, go to admin/config/development/configuration and click "view differences" next to several of the configurations.  
1. If the left and right side code is the same, but just in different position in the list, re-export config on local and push back up.
   1. Go to local.
   1. On develop, pull code and import config.  
   `git pull origin develop`  
   `px drupal cim`
   1. After import is complete, export config.  
   `px drupal cex`
   1. If there are changes to export, go ahead and commit those.
   1. Push code to origin develop.  
   `git push origin develop`  
   1. Check out master and merge deveop.  
   `git checkout master`  
   `git merge develop`
   1. Push code to origin master.  
   `git push origin master`
1. Go to Pantheon Dev and verify that config is imported on this page: admin/config/development/configuration

### Issues Deploying to Live

"Error: The website encountered an unexpected error. Try again later."
- This error can happen when configurations aren’t imported.
- If the site goes unresponsive the only way to interact with it, is using Drush via terminus. For Pr0ject-X, Travis built in terminus commands.

Step-by-Step Fix:
1. Check if the site schema has been updated as this can cause fatal errors because queries are more or less breaking because it can’t find database tables.  
`px pantheon:drupal updb`
1. If that doesn’t work then try reimporting the configuration again.  
`px pantheon:drupal cim`
1. After importing you’ll need to clear the cache.  
`px pantheon:drupal cr`
