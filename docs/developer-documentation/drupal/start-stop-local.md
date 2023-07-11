---
sidebar_position: 3
---

# Start and Stop Local Dev

We're using Project-X as a wrapper around DruaplVM.

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

### Error says there's already an npl.test
```
px env:destroy
px env:up
```

### Accidentally deleted the .vagrant folder

First, don't ever delete the .vagrant folder! You can’t delete the .vagrant folder because that’s where vagrant/VM places all it’s metadata. Removing that folder removes the association between project-x and the VM.

If you accidentally remove the .vagrant folder, do the following:
   - Destroy the Pr0ject-X environment:  
   `px env:destroy`
   - Open VirtualBox and verify that the VM is gone.
   - Go to home directory and verify that The VM is gone from VirtualBox VMs. If the VM is still there, delete it.
   - Rebuild the Pr0ject-X environment:  
   `px env:up`

## Stop Local Development Environment

1. Make sure you're in the site folder.  
`cd ~/Sites/npl-d8/`
1. Make sure all work is exported and committed.
1. Stop the environment engine.  
`px env:down`
