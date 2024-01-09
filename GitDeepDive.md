# DevOps

## Git

### Types of Version Control Systems

#### Local Version Control System:

For projects with only 1 user.
Basically timestamped copies of files.

#### Centralized Version Control Systems:

Server contains the main repository.
Server acts as the source of truth.
Only one User can modify a file at the same time.

#### Distributed Version Control Systems:

No one source of truth. Every user has a full copy of the repository.

### Centralized vs Distributed

Centralized:
- one source of truth
- user needs to connect to server (no offline work)
- only one user may edit a file at the same time

Distributed:
- everybody has the whole repository
- offline work
- many workflow possibilities

### Structure of a GIT project

#### Working Tree

Currently active checkout of a commit.

#### Staging area

Stores staged files.
Files which go into your next commit.

#### .git Directory (Repository)

Contains the whole git repository, including metadata and object database.

### GIT branching

A branch is just a pointer to a commit. 
The HEAD pointer points at the active branch.
Branches allow for diverging code paths and parallel work on the same files.

### Remote Repositories

A version of a git repository hosted on a server.
Typically only contain the .git directory (do not have a working tree).

git init --bare

### GIT Tags

Marks specific point in the history.

2 types of tags:
- lightweight: just a pointer to the commit
- annotated: object in the git database, contains tagger name, e-mail, date + message

### GIT Hooks

Scripts that run automatically at certain events.
Used to enforce commit policies or implement continous workflow.

#### GIT Local hooks:
- pre-commit
- pre-commit-message
- commit-msg
- post-commit

#### GIT Server hooks:
- pre-recieve
- update
- post-recieve