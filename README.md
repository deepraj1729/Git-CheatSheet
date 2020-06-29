# Git-CheatSheet
`Git` is the free and open source distributed version control system that's responsible for everything GitHub
related that happens locally on your computer. This cheat sheet features the most important and commonly
used Git commands for easy reference.     `#Reference from Github CheetSheet`


# Install Git:
Download Latest version of Git [Here](https://git-scm.com/downloads)

# SETUP: 
Configuring user information used across all local repositories in Terminal/Bash:

#### i.   Set a name that is identifiable for credit when review version history

      git config --global user.name “[firstname lastname]”
#### ii.  Set an email address that will be associated with each history marker

      git config --global user.email “[valid-email]”
#### iii. Set automatic command line coloring for Git for easy reviewing

      git config --global color.ui auto
      
# SETUP & INIT:
Configuring user information, initializing and cloning repositories

#### i.   Initialize an existing directory as a Git repository

      git init
#### ii.  Download an entire repository from a hosted location via URL

      git clone [repo url]

# STAGE & SNAPSHOT:
Working with snapshots and the Git staging area

#### i.   Show modified files in working directory, staged for your next commit

      git status
#### ii.  Add a file as it looks now to your next commit (stage)

      git add [file]
#### iii. Unstage a file while retaining the changes in working directory

      git reset [file]
#### iv.  Difference of what is changed but not staged

      git diff
#### v.   Difference of what is staged but not yet commited

      git diff --staged
#### vi.  Commit your staged content as a new commit snapshot

      git commit -m “[descriptive message]”

# INSPECT & COMPARE:
Examining logs, diffs and object information

#### i.   Show the commit history for the currently active branch

      git log
#### ii.  Show the commits on branchA that are not on branchB

      git log branchB..branchA
#### iii. Show the commits that changed file, even across renames

      git log --follow [file]
#### iv.  Show the diff of what is in branchA that is not in branchB

      git diff branchB...branchA
#### v.  Show any object in Git in human-readable format

      git show [SHA]

# TRACKING PATH CHANGES:
Versioning file removes and path changes

#### i.  delete the file from project and stage the removal for commit

      git rm [file]
#### ii.  Change an existing file path and stage the move

      git mv [existing-path] [new-path]
#### iii. Show all commit logs with indication of any paths that moved

      git log --stat -M

# IGNORING PATTERNS
Preventing unintentional staging or commiting of files

#### i.   Save a file with desired paterns as .gitignore with either direct string matches or wildcard globs
`logs/`
`*.notes`
`pattern*/`

#### ii.  System wide ignore patern for all local repositories

      git config --global core.excludesfile [file]

# SHARE & UPDATE:
Retrieving updates from another repository and updating local repos

#### i.   Add a git URL as an alias

      git remote add [alias] [url]
#### ii.  Fetch down all the branches from that Git remote

      git fetch [alias]
#### iii. Merge a remote branch into your current branch to bring it up to date

      git merge [alias]/[branch]
#### iv.  Transmit local branch commits to the remote repository branch

      git push [alias] [branch]
#### v.   Fetch and merge any commits from the tracking remote branch

      git pull

# REWRITE HISTORY:
Rewriting branches, updating commits and clearing history

#### i.   Apply any commits of current branch ahead of specified one

      git rebase [branch]
#### ii.  Clear staging area, rewrite working tree from specified commit

      git reset --hard [commit]

# TEMPORARY COMMITS:
Temporarily store modified, tracked files in order to change branches

#### i.   Save modified and staged changes

      git stash
#### ii.  List stack-order of stashed file changes

      git stash list
#### iii. Write working from top of stash stack

      git stash pop
#### iv.  Discard the changes from top of stash stack

      git stash drop

