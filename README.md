# Git

  * Initialize repository: ```git init```
  * Set username globally: ```git config --global user.name "userName"```
  * Set email globally: ```git config --global user.eamil "userEmail@email.com"```
  * View userName, email: ```git config --list```
  * View tracked or untracked files: ```git status```
  * Add a file to staging area: ```git add <<fileName>>```
  * Add all files to staging area: ```git add .``` or ```git add --all```
  * Remove files from staging area: ```git rm --cached <<fileName>>```
  * Delete a file from local repo, all stages: ```git reset HEAD <<fileName>>``` 
  * Commit files to local repository: ```git commit -m "<<commit message>>"```
  * View all the commit messages in descending order: ```git log```
  * View all the commit messages in a cleaner way: ```git log --oneline```
  * Suppose, there are 3 commits. But, the 3rd commit was made accidentally i.e. there was some bug in that code thats why we need to go back to the 2nd commit. [Here, 2nd commit means where codebase was bug free. 3rd commit means, someone made some change in codebase and committed that buggy code]: ```git checkout <<2nd commit id>>``` 
  * View difference between working directory and staging area: ```git diff```
  * We can't see the difference after we make "git add" command. Because, "git diff" is used to see the differences between working directory and staging area. But, If we want to see the differences even after "git add", use ```git diff --staged``` 
  * View the changes of a commit i.e. which files and contents were changed during that commit: ```git show <<commitID>>```
  * Compare code changes of two commits: ```git diff commit1ID commit2Id```
  * Push an existing local repository to remote repo i.e. Github: ```git remote add origin <<git remote repo url>>``` then ```git push -u origin master```
  * **SSH key**: Add SSH key to any repo, then if anyone want to commit to this repo, no username and password will be required. 
  * **SSH key generation**: 
     - ```ssh-keygen -t rsa -b 4096 -C "<<useremail>>"``` then enter key name and passphrase. one .keys and one .keys.pub file will be generated.
     - ```eval $(ssh-agent -s)``` -- We'll get an Agent pid
     - ```ssh-add ~/.ssh/id_rsa``` -- We'll need to provide the password which we'd provided in the 1st phase
     - Now, copy the SSH key to clipboard: ```clip < ~/.ssh/id_rsa.pub```
  * **Add this SSH key to reporsitory** : Github -> settings -> SSH and GPG keys -> new SSH key -> enter title and paste the key -> Add SSH key
  * Download any project from github to local working directory: ```git clone https://github-repo-url```
  * Create a branch for a project: ```git branch <<branchname>>```
  * Show total branches: ```git branch```
  * Switch to any branch: ```git checkout <<target branch>>```
  * Create and Swtich to a branch at a time: ```git checkout -b <<newBranchName>>```
  * Suppose, we are in master branch. We need to bring some changes from a child branch to master: ```git merge childBranch```. If we want to bring some changes from master to child, ```git checkout child``` then ```git merge master```
  * Delete a branch: ```git branch -D branchName```
  * Temporary put some code before commit in any isolated area where git will not track and we can get it back anytime we want, stash it: ```git stash```
  *  To recover those code: ```git stash pop```
  *  To view all stashes: ```git stash list```
  *  To recover any particular stash: ```git stash pop <<stashSerialNumber>>```
  *  To delete all untracked files: ```git clean -f```
  *  To see a confirmation before deleting: ```git clean -f -n```
  
