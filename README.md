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
    - A commit message should be brief
    - Github truncates a commit message after 69 characters thereabout so keep it brief in order not to make people guess what the remaining words would be
    - If you need to explain further, use a description which should explain the context
    - Commit message should be in the future tense (fix vs fixed)
    - Commit message should encapsulates one idea (single responsibility)
    - Commits should generally leave your branch in a clean state, (tests should pass)
* `git checkout -`  Checkout to the previous branched
