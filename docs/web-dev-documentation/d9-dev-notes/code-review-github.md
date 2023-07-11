---
sidebar_position: 6
---

# Code Review in Github

Before merging code into master, you must request code review from another team member.

1. Request review by an Aten or NPL team member.
1. Reviewer approves or rejects changes in Github.
   1. Reviewer can approve changes, which turns the merge button green.
   1. Reviewer can reject changes and add comments for things that need to be changed.
1. Follow the next step based on whether changes were accepted or rejected.

## If Changes are Accepted (Approved Pull Request)

1. Comment on the pull request in Github and approve.
1. See [Deploy to Production](/docs/d9-dev-notes/deploy-code-production/) for next steps.

## If Changes are Requested During Review

Only do this process if the reviewer flagged issues that need to be addressed before merging.

1. If the branch is already on your local, check it out:  
`git checkout feature/NPLD8-xx`
1. If the branch was created by someone else:
   1. First, fetch code:  
   `git fetch --all`  
   1. Second, check out the feature branch:  
   `git checkout feature/NPLD8-xx`  
   1. Last, pull code:  
   `git pull origin feature/NPLD8-xx`
1. Import config to get environment back to state of those features:  
`px drupal cim`
1. Fix issues and commit your changes.
   1. If there are configurations that don’t belong, just don’t add to the commit.
   1. You can rm untracked files or checkout -- the configs you didn't need.
1. Export config:  
`px drupal cex`
1. Push your changes back up to the feature branch:  
`git push origin feature/NPLD8-xxx -f`
1. Once the build process is complete, request review of changes again.
1. Once changes are approved, follow steps above for an approved pull request.
