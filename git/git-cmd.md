
## Git CMDs
Remove added file:
>git reset \<file-path\>  
>git rm --cached \<file-path\>

Add origin to remote repository
>git remote add origin \<https://github.com/JxSrcInc/help.git\>

push local to remote
>git push -u origin master


Change the branch name you on
>git branch -m \<new-name\>

Change to a different branch name
>git branch -m \<old-name\> \<new-name\>

Delete remote branch
>git push -d \<remote\> \<remote branch\> -: git push -d origin feature/tmp

[Delete a remote GIT Branch](https://koukia.ca/delete-a-local-and-a-remote-git-branch-61df0b10d323)
>git push _remote-name (origin)_ -d _branch-name (develop)_

[Inspecting a Remote](https://www.atlassian.com/git/tutorials/syncing) to get a list of branches associated with the remote and also the endpoints attached for fetching and pushing
>git remote show _remote-name (origin)_

Undo tracked file (undo add command)
>git reset