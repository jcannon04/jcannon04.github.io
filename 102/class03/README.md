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

`git revert HEAD` will "undo" the latest commit. It actually creates a new commit, appends it and rolls back the changes from an specified commit in this case `HEAD`. Any commit in the history of the repo can be specified.

**Unmodifying a file**

`git checkout -- filename`  will return the file specified back to it's state in the latest commit.

## Branching

Almost every type of version control system includes branchine. Branching allows for multiple collaborators to work on the same repository at the same time in different branches and not affect the main repository. A collaborator can create a branch, work in that branch, switch between branches and merge branches. A git branch is like a pointer that points to the most recent commit. The HEAD is a special pointer that indicates which branch your currently working in.

**Creating a new branch**

The command `git branch [branch name]` will create a new branch pointing to your most recent commite but will not switch to it.

**Switching branches**

`git checkout [branch-name]` will point the head to your the name branch. If you commit to the new branch the branch you checked out from will still be pointing to the last commit you made before checking out. So, if you switch back to the original branch you will not see the changes that were made in your new branch.

**Create a new branch and checkout**

You can create a new branch and check it out in one line with the `git checkout -b [branch-name]` command.

**List branches**

`git branch` will list all available branches.

## Merging

Use `git merge` to merge changes from another branch into your current one

**Fast-forward merging**

In fast-forward merging the pointer from your current branch is moved up to the last commit of the branch that you are merging with yours. There is no divergent work the latter brach is directly upstream from yours.

**Not fast-forward** 

`git merge --no-ff <branch>` with no fast-forward instead of simply moving your current pointer up a new commit is created. Used to prevent data loss about merges and branches.

**Three-way merge**

In the case of branches diverging a fast-forward commit can not be used. Involves a your working branch, the branch you are merging in and the common ancestor. Instead of moving the pointer forward a new snapshot is made and a commit that points to it. this is refered to as a merge commit and has more than one parent.

**fetch and merge**

`git pull` will fetch and merge remote changes

**Deleting branches** 

`git branch -d <branch>` will delete a branch. It is okay to do with branches that have been successfully merged

**Merge Conflicts** 

When two merged branches both have different changes in the same place in a file git can not merge then cleanly


```diff
My name is

 <<<<<<< HEAD

 Jane

 =======

 Mary

 >>>>>>> branch-test
```

HEAD marks the current checked out branch and the content above ======== lives in this branch. The content below exists in the file you are attempting to merge in to yours. After fixing the files and removing ======== and >>>>>>>>. You will be able to merge them successfully.

`git status` will show you unmerged files

**Preview Changes**

git diff <source_branch> <target_branch>

will allow you to preview changes for merging

**Listing branches**

`git branch` will list all local branches. there will be an asterisk next to the one you are currently woking on

**See latest commits**

`git branch -v` will show you the newest commits for each branch

`git branch --merged` will show you which branches you have merged into your current working branch. There will be a * next to your current working branch. Branches show in this command without a * are generally okay to delete because you have already successfully merged them and all of your work is already in your current branch.

`git branch --no-merged` shows all branches that you have not yet merged in to your current working branch

## Rebasing

TODO

## Things I Want To Know More About

* Rebasing
* Tagging
* GitHub Workflow

**resources**

[GitHub Tutorial](https://blog.udemy.com/git-tutorial-a-comprehensive-guide/#11)
