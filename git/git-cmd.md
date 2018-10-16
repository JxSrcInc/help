
## Git CMDs
Remove added file:
>git reset _file-path_  
>git rm --cached _file-path_

Add origin to remote repository
>git remote add origin _https://github.com/JxSrcInc/help.git_

push local to remote
>git push -u origin master


Change the branch name you on
>git branch -m _new-name_

Change to a different branch name
>git branch -m _old-name_ _new-name_

[Delete a remote GIT Branch](https://koukia.ca/delete-a-local-and-a-remote-git-branch-61df0b10d323)
>git push _remote-name (origin)_ -d _branch-name (develop)_

[Inspecting a Remote](https://www.atlassian.com/git/tutorials/syncing) to get a list of branches associated with the remote and also the endpoints attached for fetching and pushing
>git remote show _remote-name (origin)_
