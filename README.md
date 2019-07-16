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
    - `git branch --merged master` check branches that have been merged with master
    - `git branch --no-merged master` check branches that haven't been merged yet with master

* `git checkout -`  Checkout to the previous branched


Logs
    - `git log --since=yesterday`  # show logs for yesterday
    - `git log --since="3 weeks ago"`   # show logs for three weeks ago
    - `git log --name-status --follow --oneline filename` # this helps you check history of a file, from when the name was changed, how it was moved around etc


Referencing
    - `^` previous one
    - `^^^` last three commits
    - `^n` reference a particular commit e.g (^2), you can also use `~n`


Differences
    - `git show <commit>` show commits and its contents
    - `git show <commit> --stat` show files changed in the commit
    - `git show <commit>:<file>` look at a file from another commit
    - `git branch --merged master` check branches that were merged to master
    - `git branch --no-merged master` check branches that aren't merged with master yet
    - `git diff` Unstaged changes
    - `git diff --staged` staged changes


Fixing mistakes
    - `git checkout <deleted_commit>` to restore a deleted commit


Cleaning
    - `git clean` # to clean working area by deleting untracked files
    - use `--dry-run` to see what would be deleted
    - specify `-d` to clean directories
    - `git revert` # it will create a commit to revert the recent commit
