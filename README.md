> To initialize new .git project

`git init $projectName`

> To check status of currect project

`git status`

> To add individual files to Staged area

`git add $fileName`

> To add all files to Staged area

`git add .`

> To commit staged files on local branch

`git commit -m "$commitMessage"`

| key      | value |
| ----------- | ----------- |
| -m      | to provide commit message       |

> To view commit history of current branch

`git log`

> To view diff changes in last git commit

`git show`

> To view list of files that are tracked by git

`git ls-files`

> To directly commit all modified files without performing staged operation

`git commit -a`

> To unstage any file

`git reset HEAD $fileName`

> To undo modified changes of a file

`git checkout -- $fileName`

> To view decorated and single line git log

`git log --oneline --graph --decorate --all`

| key      | value |
| ----------- | ----------- |
| --oneline |to view everything on a single line.|
| --graph|to view asterisk based graph denoting our branched hierarchy.|
| --decorate|to view which commit are part of which branch.|
| --all|to view history of all the branches available in repository.|

> To create new alias in git

`git config --global alias.$aliasName "$gitCommand"`

| key      | value |
| ----------- | ----------- |
|--global    |to configure on global level.         |
|Example|`git config --global alias.history "log --oneline --graph --decorate --all"`|

> To call git alias

`git $aliasName`

> To view list of all global parameters

`git config --global --list`

> To edit global parameters

`git config --global -e`

> To view logs of a particular file

`git $aliasName -- $fileName`

| key      | value |
| ----------- | ----------- |
|Example	    |  `git history -- README.md`       |

> To rename a file

`git mv $oldFileName $newFileName`

> To add only updated files to staged area

`git add -u`

> To add all modified files to to staged area

`git add -A`

> To check difference in commit and HEAD

`git diff $commitId HEAD`

> To check difference between any two commits

`git diff $commitId1 $commitId2`

> To check difference between any two branches

`git diff $branchName1 $branchName2`

> To view all branches

`git branch -a`

| key      | value |
| ----------- | ----------- |
|-a    |   list both remote-tracking and local branches      |

> To checkout a new branch

`git checkout -b $branchName`

| key      | value |
| ----------- | ----------- |
|-b    |  to create and checkout a new branch       |

> To switch between branch

`git checkout $branchName`

> To merge branch

`git merge $branchName`

**Note:** _to merge newBranch with master branch, you need to switch to master branch first and then hit merge command._

> To delete a branch

`git branch -d $branchName`

| key      | value |
| ----------- | ----------- |
|-d    |  to delete a particular branch.       |

> To view merging conflicts in a file

`cat $fileName`

> To create new tag

`git tag $tagName`

> To view all created tags

`git tag --list`

> To delete a tag

`git tag -d $tagName`

> To create annotated tags

`git tag -a $tagName -m "$message"`

| key      | value |
| ----------- | ----------- |
|-a    |  to denote annotated tags.       |
| -m   |  to add message to this tag.       |
|   Example | `git tag -a v1.0 -m "Release 1.0"`        | 

> To view information of any tag

`git show $tagName`

> To create a tag for a branch

`git tag $tagName $branchName`

**Note:** _this tag will be linked with the current HEAD of $branchName_

> To create a tag for a commit

`git tag -a $tagName -m "$tagMeaasge" $commitId`

> To delete a tag remotely

`git tag -d $tagName`

`git push origin :$tagName`

| key      | value |
| ----------- | ----------- |
|:$tagName    |':' denotes to delete from remote repo.         |

> To update tag reference to new commit

`git tag -f $tagName $commitId`

| key      | value |
| ----------- | ----------- |
|-f    |  to force update current reference of tag to new commit id       |
|  Example  | `git tag -f stable 9ed6d70`        | 

> To push updated tag reference to new commit

`git push --force --tags`

> To push single tag to remote repository

`git push origin $tagName`

> To stash local changes

`git stash`

> To view all stashes

`git stash list`

> To restore stash to branch

`git stash pop`

> To reset HEAD to a previous commit

`git reset $commitId --soft`

`git reset $commitId --mixed`

`git reset $commitId --hard`

| key      | value |
| ----------- | ----------- |
|--mixed    |it is default behaviour of reset command.         |

**Note:** _In soft and mixed reset, we'll have files in our staged/unstaged area but in hard reset there will be no staged/unstaged files._

> To view log of all actions taken in an repository

`git reflog `

> To link local repository with remote repository

`git remote add origin $remoteURL`

> To push local code to remote repository

`git push -u origin $branchName --tags`

| key      | value |
| ----------- | ----------- |
|-u    |  it sets up branch tracking relationship between remote and local branch.       |
| --tags   |  to push all tags.       |
| origin   |  name of remote reference.       |
| Example   | `git push -u origin master --tags`        |

> To clone repository from GitHub

`git clone $cloneUrl`

**Note:** _it will create a folder in local system with same name as our repository name._

> To clone repository from Git with custom local folder name

`git clone $cloneUrl $folderName`

> To fetch all changes from GitHub

`git fetch`

> To pull all changes from GitHub

`git pull`

**Note:** _internally pull command is combination of fetch and mege command._

> To remove any file

`git rm $fileName`

> To remove delete branches stale reference from branches list

`git fetch -p`

| key      | value |
| ----------- | ----------- |
|-p    |  It looks for any dead branches on git and remove those branches reference from local repository.       |

> To update/pull all local branches in a single command

`git pull --all`

> To delete a remote branch from local system

`git push origin :$branchName`

| key      | value |
| ----------- | ----------- |
|:$branchName    |It ':' tells git to delete remote branch with specified $branchName         |

> To keep your local branch ahead of origin/master

`git pull --rebase`

| key      | value |
| ----------- | ----------- |
|--rebase    | Rebase first rewinds your local branch i.e. it undo's all your local changes, then it brings all changes from Github and then it applies all local changes back to that branch to stay ahead of master.       |  
			  
