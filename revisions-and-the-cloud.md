# Revisions and The Cloud

## Version Control

Version control systems allows you to keep track of changes in a file or set of files. They allow you to see what changes have been made over time and enable yo to
revert to an older version if need be. 

### Local Version Control

older VCS were local meaning there was only one database on your local computer to track changes

### Centralized Version Control

Centralized Version Control Systems allowed collaboration by storing the files on a server and allowing everyone on the same project to see others work and they
allowed administrator to divy up the work more efficiently. Central server instead of a collection of local databases

### Distributed Version Control

Addresses the major issue with a CVS. All the files for a project on a server creates a single point of failure and can result in catostropic loss of data.
DVCS creates back ups mirrors of the project to reduce the chance of loosing data.

## So, What Is Git?

### Snapshots

Git is a DVCS that makes snapshots of your project. Every time you update with a commit git stores a reference to the project so you can return to a previous version if you make a change that breaks something

### Local Operations

Git relies mostly on local operations and local resources. You can pull the project into your local environment and not have to rely on staying connecting on the internet to make changes

### Tracking Changes

Git keeps track of every change made in every file and warns you of file corruptions and other file issues

### Loss of Data

Git makes it extremely difficult to lose data. It is very unlikely that a commit will get lost

### States

Git has files have 3 main stage. Staged, Modified, Commited. Commited files are securely stored in a local database. Modified files have been changed but not commited to database. Staged files version have been flagged to be commited in the next snapshot

