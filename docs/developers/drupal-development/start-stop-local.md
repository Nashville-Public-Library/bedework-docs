# Start and Stop Local Dev

We're using Project-X as a wrapper around DDEV.

## Start Local Development Environment

1. Open terminal.
1. Go into site root folder.  
`cd ~/Sites/npl-d8`
1. Start the environment engine.  
`px env:up`
1. You should see "Launch the environment? (y/n)." Type yes.  
`yes`
1. You may get prompted for your computer password.

## Troubleshoot Start Up

Removed VirtualBox info. No other troubleshooting info available.

## Stop Local Development Environment

1. Make sure you're in the site folder.  
`cd ~/Sites/npl-d8/`
1. Make sure all work is exported and committed.
1. Stop the environment engine.  
`px env:down`
