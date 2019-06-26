#### GTI CHEATSHEET

I made this git cheatsheet for myself to save most of the git commands I use.

***

Checking what will be staged to the staging area interactively
* `git add -p`

Remove file from staging area
* `git reset filename`

Stash with a descriptive name
* `git stash save "descriptive message"`

Lists all the stash made
* `git stash list`

Show the content of a stash
* `git stash show`  # for recent stash
* `git stash show stash@{stash_number}`  # show specific stash

Applying a stash
* `git stash apply`  # apply last stash
* `git stash apply stash@{stash_number}`   # apply specific stash

Avoid resolving merge conflicts and rebase all the time
* `git config rerere.enabled true` turn on git rerere for the project, pass --global to enable for all projects

    - This will use the first step in resolving a conflict for future conflicts

Branches
* `git checkout -`  Checkout to the previous branched