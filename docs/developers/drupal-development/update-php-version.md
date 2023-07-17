# Update PHP Version

1. Create a new feature branch, you haven't already.   
    1. Be sure to pull code before making the feature branch.  
    1. Be sure to import config after making the feature branch.  

1. Open the following files in your text editor:
    1. pantheon.yml  
    1. project-x.yml  
    1. .circleci/config.yml    
    1. .ddev/config.yaml  

1. Change the php version in the files, then save.  
    1. Update php in pantheon.yml   
    ![Local Settings](/img/php-update-1.png)
    1. Update php in project-x.yml  
    ![Local Settings](/img/php-update-2.png)
    1. Update php in .circleci/config.yml    
    ![Local Settings](/img/php-update-3.png)
    1. Update php in .ddev/config.yaml  

1. Open the composer.json file. Update php under config>platform. Save.  
```
"config": {  
  "platform": {  
    "php": "8.0"  
  },  
```

1. Because we updated the composer.json file we need to update the lock file:  
`composer update --lock`

1. Check the status:  
`git status`

1. Add the files and commit work.

1. Because we updated the config.yml in DDev, we need to make DDev recognize the update.    
`px env:init`

1. Now restart Project-X.  
`px env:restart`  

1. Check to verify that PHP is updated locally. The config change to the DDev config.yml file should update local environment.

1. If PHP is updated locally, push changes to your feature branch.

1. Approve the pull request or have someone else approve it.

1. Now we have to do steps to force Pantheon to recognize the update we just made.
    1. Open the composer.json file and make a change to one of the comments.
    1. Commit changes.
    1. Push to feature branch.

1. Check to verify that PHP is updated on your feature branch. If it is, you can merge the pull request into develop.

1. After merging into develop, follow deploy steps as you do in other branches.
