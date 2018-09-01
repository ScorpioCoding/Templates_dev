# Templates

Read the wiki for Concept and Design

### Template github Repo's

1.  Template development [dev] : https://github.com/ScorpioCoding/Templates_dev.git
2.  Template publish on github pages [pub] : https://github.com/ScorpioCoding/Templates.git

==> ALL DEVELOPMENT IS DONE IN THE [dev] REPO !!

### Dev repo Branches

1. `master` - fixed branch - holds only releases
2. `dev` - fixed branch - is the main dev branch [ clone & pull request go here ]
3. `hotfix` - temp branch - for errors on the master branch [ merged to master & dev ]
4. `fix` - temp branch - for errors on the dev branch [ merged to dev only ]
5. `feature` -temp branch - for new milestones, idea's, testcases, etc. [merged to dev only]

### Git Rules for the `dev` repo

1. The `master` branch is off limits and holds only release commits.
2. The `dev` branch is the main development branch where everyone clones from and PULL requests are issued to.
3. Clone the `dev` branch and then..  
   -- use `$git checkout <existing branch>` to switch to an allready created branch  
   -- use `$git checkout <new branch> -b` to switch and create the new branch
