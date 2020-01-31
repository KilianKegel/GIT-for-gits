# GIT-for-gits
HowTo GIT for me, myself and IT
### miscellaneous
* `git branch -a` -> list all branches<br>
* `git push -u origin BRANCHNAME` -> push new branch remotely/upstream<br>
* `git checkout BRANCHNAME/HASH` -> switch to branch<br>
* `git merge BRANCHNAME/HASH` -> automatic merge<br>
* `git mergetool` -> merge manually
* `git submodule update --init --recursive`
* `git reset --hard` -> last commited state of entire repository
* `git log --simplify-by-decoration` -> list branches and tags only
* `git fetch`
* `git pull`

### exchange a submodule
1. `git submodule deinit SUBDIR`
2. `git rm --cached SUBDIR`
3. `rd /s /q .git\modules\SUBDIR`
4. `rd /s /q SUBDIR`
5. `git submodule add <URL> SUBDIR`

### move/upload locale GIT repo to GitHub
1. `git remote -v`        -> list remotes
2. `git remote rm origin` -> delete origin
3. `git remote add origin <remote URL>` -> assign new origin
4. `git pull --allow-unrelated-hisories`
5. `git push origin HEAD:master`
