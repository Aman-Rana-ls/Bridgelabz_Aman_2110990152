6. git merge branchname = Go to the main branch (or any branch you want to merge into) and merge the specified branch (branchname) into it.

7. to push git init # Initialize Git (if needed) git add # Stage the file git commit -m      "message" # Commit changes git remote add origin # Link to GitHub or git add origin main    for already config with github git push -u origin main # Push to GitHub

8. pull git pull origin main

9. git clone git clone is to use if you want to take particular branch clone in you local repo and if you want to take clone of the project

10. git diff ../ to check diff b/w local and remote

11. fetch vs pull fetch = it is used to fetch remote project in local repo but it is not    merge in local repo it is for to show you the if difference b/w the local repo and remote repo if we want to take the remote repo then we have to merge the repo git diff ../ to check difference git merge origin/main This will merge the changes fetched from the remote branch (origin/main) into your local main branch.

pull = it is used to fetch and merge the repo 

12. Summary of git diff Use Cases: Unstaged Changes (working directory vs staging area):

bash Copy code git diff Staged Changes (staging area vs last commit):

bash Copy code git diff --cached Compare Two Branches:

bash Copy code git diff branch1..branch2 Compare Local Branch with Remote:

bash Copy code git diff branch..origin/branch

13.Purpose of git stash -u By default, when you run git stash, it only stashes the tracked changes (i.e., files that are already being tracked by Git). However, if you have untracked files (files that are not added to the staging area or tracked by Git), they are not included in the stash.

When you use git stash -u (or git stash --include-untracked), it also stashes the untracked files, allowing you to temporarily save them along with the changes in your tracked files. Syntax bash git stash (default): Stashes only tracked files. git stash -u: Stashes tracked and untracked files. git stash -a: Stashes tracked, untracked, and ignored files. git stash list Lists all stashes git stash show <stash@{n}> Shows a summary of a specific stash git stash show -p <stash@{n}> Shows a detailed diff of a specific stash git stash apply Applies the most recent stash without removing it from the stash list git stash apply <stash@{n}> Applies a specific stash without removing it from the stash list git stash pop Applies and removes the most recent stash git stash pop <stash@{n}> Applies and removes a specific stash git stash drop <stash@{n}> Removes a specific stash without applying it git stash clear Removes all stashes git stash save "message" Stashes changes with a custom message