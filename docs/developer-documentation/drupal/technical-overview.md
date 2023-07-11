---
sidebar_position: 1
---

# Technical Overview: Github, CircleCI, Project-X, Pantheon

NPL-D8 project workflow allows multiple developers to work on site features simultaneously without conflict.

## Git Branches

- Feature branches are where we do work.
- Develop branch is where we collect features to prepare for a release.
- Master is the stable release branch.

## Workflow Overview

- Developers use git flow to crate feature branches.
- Work is done on the feature branch then pushed to Github where CircleCI creates a Pantheon multidev.
- Work is tested on the multidev. If the multidev looks good, developer creates a pull request in Github.
- Work is reviewed in Github and, if approved, it is merged into develop.
- Develop is then merged into master which is pushed up to Github. Github does the build and deploy to get changes to Pantheon dev.
- Work is reviewed on Pantheon dev and test before being deployed to live.

## Key Items for Building the Workflow

- Github > *SSH Key for Pantheon AND CI user in Pantheon*
   - This is a fragile point in the workflow. Currently, ci@atendesigngroup.com has to be a developer on the Pantheon project. If the user is removed from the group in Pantheon, then all of CircleCi will break (pushing code will break). We can swap out that user to an NPL email if we want.
   - If we move to an NPL ssh key, we’d need to update that in the .circleci > config.yml file in two places.

- CircleCi > *Pantheon Machine Token*
   - In "environment variables" on circleci.com, tell CircleCI the Pantheon machine token.

- CircleCI YML Configs > *npl-d8 > .circleci > config.yml*
   - Documentation on CircleCI on configurations.
   - One job is to build everything, run composer, packages all that stuff into a workspace. Can deploy a package to a PR or do a development deployment.
   - If pull request is open or feature branch is created, there are deployment steps that happen. Those are defined in the config.yml file.
   - Info on creating a multidev site based on the feature branch name.

- Project-X Build Options > *project-x.yml*
   - Has build options for the project, rather than putting those in .circleci > config.yml. Copies a bunch of files over to the build, runs composer update.
   - SSH Path for Pantheon Dev site: States where the repo is, includes the long ssh path to get code in Pantheon.
   - Plugin configurations saying project defaults. Connected to Jira board.

- Pantheon YML Configs > *pantheon.yml*
   - Pretty bare bones.
   - Telling what happens after a deploy and after a code sync.
   - Calls a file called afterSync.php
   - All documented on Pantheon for this thing called Quicksilver, which was used for the afterSync.php code.

- Slack > CirlceCI Plugin
   - Aten set up a Slack + CircleCI plugin. See if we can do that on NPL Slack.

## Issues / Troubleshooting:
You can circumvent CircleCI if it is down and you need to deploy asap. See: https://github.com/Nashville-Public-Library/npl-d8#local-deployment
