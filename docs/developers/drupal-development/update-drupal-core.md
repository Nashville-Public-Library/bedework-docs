# Update Drupal Core

## Background

- On Drupal 7, Pantheon developers would update Drupal core on all their sites. Pantheon developers did the hard work, resolved conflicts, then users could click a button to apply the update Pantheon installed.

- On Drupal 8, we used Composer and an empty upstream because Pantheon didn't have an upstream for Composer-managed sites. We also used Github and a build process. For those reasons, we have to do the update and apply patches ourselves.

- On Druapl 9 and 10, we're still using Github and a build process, so we're still updating and applying patches ourselves.

- In composer.json, we have "drupal/core-recommended": "9.2.0 as 8.9.0" which is needed for all contributed modules that have not officially been updated to D9 and were just updated via patches.

## Step-by-Step

1. Checkout develop:  
`git checkout develop`
1. Pull code:  
`git pull origin develop`
1. Create a new feature branch for the ticket:  
`git flow feature start NPLD8-xxx`
1. Import config:  
`px drupal cim`
1. Run the update command:  
`composer update drupal/core-recommended --with-all-dependencies`
    1. In composer.json, we have "drupal/core": "9.2.0 as 8.9.0" which is needed for all contributed modules that have not officially been updated to D9 and were just updated via patches.
    1. If you update it to 9.2.1 and then rerun the command composer update drupal/core "drupal/core-*" --with-all-dependencies" it should work.`
1. If you get a memory size error, update the memory limit for this session. The COMPOSER_MEMORY_LIMIT environment variable, with value set to -1, adds more memory to the current Terminal session. It will be used by all the composer commands you use in that session. [Get more info.](https://www.agileana.com/blog/composer-memory-limit-troubleshooting)  
`export COMPOSER_MEMORY_LIMIT=-1`
1. When the update command is done, run the database update command. This goes through all the updates, looks at any schema changes happening in the database, and lets you know what they all are.  
`px drupal updb`
1. Type yes to run the updates.
1. Clear cache:  
`px drupal cr`
1. Export configuration to make sure there were no changes we need to commit. You don't have to do every time, but if there's a problem this is a good thing to check.  
`px drupal cex`
1. Check status.  
`git status -s`
1. If there were changes, commit those changes.
1. Test on your local environment.
1. Push to multidev.
1. Test on the multidev.
1. Prior to merging into master and pushing code to Pantheon, take a database snapshot on Live in case updates don’t work. That allows you to roll back quickly.  

See [Github Code Review](/docs/d9-dev-notes/deploy-code-production/) for next steps.
