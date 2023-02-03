# Revisions and The Cloud

## Version Control

Version control systems allows you to keep track of changes in a file or set of files. They allow you to see what changes have been made over time and enable you to revert to an older version if need be.

**Local Version Control**

Older VCS's were local meaning there was only one database on your local computer to track changes

**Centralized Version Control** (CVCS)

Centralized Version Control Systems allowed collaboration by storing the files on a single server and allowing everyone on the same project to see others work. They also allowed administrators to divy up the work more efficiently. An improvement from a single database for each indivudual. Uses a central server instead of a collection of local databases

**Distributed Version Control** (DVCS)

Addresses the major issue with a CVS. All the files for a project on a server creates a single point of failure and can result in catostropic loss of data. DVCS creates back ups mirrors of the project repositories to reduce the chance of loosing data. Also having mirrored repositories allows for multiple individuals with different workflows to work on the same project.

## What is Git?

**snapshots*

Git is a DVCS that makes snapshots of your project. Every time you update with a commit git stores a reference to the project so you can return to a previous version if you make a change that breaks something

**Local Operations**

Git relies mostly on local operations and local resources. You can pull the project into your local environment and you don't have to rely on staying connected on the company’s vpn or other services in order to work on the project

**Tracking Changes**

Git keeps track of every change made in every file and warns you of file corruptions and other file issues

**Loss of Data**

Git makes it extremely difficult to lose data. It is very unlikely that a commit will get lost

**States**

Git files have 3 main stages. Staged, Modified, Committed. Committed files are securely stored in a local database. Modified files have been changed but not committed to database. Staged files version have been flagged to be committed in the next snapshot

## Getting Started

For a quick guide to getting a git repository set up on your device see [this article](https://blog.udemy.com/git-tutorial-a-comprehensive-guide/#4)

## Workflow

**Local Repository Structure**

Your local git repository has three main components

1. Working Directory - all projects files live here
2. Index - area used for staging
3. Head - points to the most recent commit

**Saving Files**

Files in a git repository have two possible states 

1. Tracked - files were included in last snapshot and can modified, unmodified or staged
2. Untracked - were no included in last snapshot and are not in the staging area

**File Status LifeCycle**

When you edit a file it becomes modified. You can then stage the modified file. Then you commit the saved changes

**File Status Check**

you can check the status of your files with `git status` 

**Tracking and staging files**

you can track and stage a file with `` git add `file name` ``

you can also use `git add *` to add all files in repository

`git status` will then update to tell you which files are ready to be committed

**Committing Changes** 

`$ git commit -m “made change x, y, z”` will commit staged changes

you can use `commit -a` to add all modified and tracked files to the snapshot

**Pushing Changes**

`$ git push origin master` pushes your changes to the remote repository

Origin is the default name for your remote repository. Master is the name of your current local branch

**Stashing Changes** 

`git stash` allows you to save changes for later. It removes changes and hides them giving you a clean working directory. To start working on the changes again use `git stash apply`

## Remote Repositories

In order to collaborate with others you must interact with remote repositories below are some way to do just that

**Adding Remotes**

The `git remote` command will show all of your remote repos' short names use `git remote -v` to also show the urls

You can create new remote repos with this format `git remote add short name url`

**Fetching**

`git fetch [remote-name]` will get the data that has changed since you cloned or last fetched your project from remote repos into your local project. It does not modify your local work or merge your changes.

**Pushing**

`git push [remote-name][branch-name]` will push your changes upstreaming for sharing. You can only use push if you have write access to the remote repo and you have pulled and merged ass changes since the last push.

**Renaming and Removing**

use `git remote rename [old name] [new name]` to rename remote repo
use `git remote rm [repo name]` to remove remote repo

## Undoing Actions

**Commit Mistakes**

`git commit --amend` allows you to make changes to the last commit such as staging a file, or changing the commit message

**Unstaging a File**

`git reset HEAD [filename]` will remove a file  from the staging area

**Undo a Committed Snapshot**

`git revert HEAD` will "undo" the latest commit. It actually creates a new commit, appends it and rolls the back the changes from an specified commit in this case `HEAD`. Any commit in the history of the repo can be specified.

**Unmodifying a file**

`git checkout -- filename`  will return the file specified back to it's state in the latest commit.

## Branching

TODO

## Things I Want To Know More About

* Merging and Branching
* Rebasing
* Tagging
* GitHub Workflow

**resources**

[GitHub Tutorial](https://blog.udemy.com/git-tutorial-a-comprehensive-guide/#4)

