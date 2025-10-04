# GIT-for-KGits
HowTo GIT for me, myself and I . . .
### miscellaneous
* `git branch -a` -> list all branches<br>
* `git push -u origin BRANCHNAME` -> push new branch remotely/upstream<br>
* `git checkout BRANCHNAME/HASH` -> switch to branch<br>
* `git checkout <HASH> -- file.c` -> checkout a specific version of a file.c
* `git merge BRANCHNAME/HASH` -> automatic merge<br>
* `git mergetool` -> merge manually
* `git submodule add <URL> <SUBDIR>`
* `git submodule update --init --recursive`
* `git -c submodule.UnitTestFrameworkPkg/Library/SubhookLib/subhook.update=none submodule update --init --recursive` -> skip broken submodule UnitTestFrameworkPkg/Library/SubhookLib/subhook
* `git reset --hard` -> last commited state of entire repository
* `git reset <PATH\FILE>` -> unstage a particular file
* `git log --simplify-by-decoration` -> list branches and tags only
* `git fetch`
* `git pull`
* `git checkout --patch BRANCHNAME file` -> merge a single file from a different branch
* `git tag <tag_name>` set tag_name
* `git tag -a <tag_name> -m "message"`
* `git tag` list tags
* `git push --tags`
* `git push origin --delete main` -> delete remote branch main

### upload repo to new remote URL
* `git remote set-url origin <REMOTEURL>`

### ignoring submodule changes in a superproject
1. git config -f .gitmodules submodule.SUBMOD.ignore dirty
2. git submodule sync --recursive

### exchange a submodule
1. `git submodule deinit SUBDIR`
2. `git rm --cached SUBDIR`
3. `rd /s /q .git\modules\SUBDIR`
4. `rd /s /q SUBDIR`
5. `git submodule add <URL> SUBDIR`

### move/upload local GIT repo to GitHub
1. `git remote -v`        -> list remotes
2. `git remote rm origin` -> delete origin
3. `git remote add origin <remote URL>` -> assign new origin
4. `git pull --allow-unrelated-hisories`
5. `git push origin HEAD:master`
