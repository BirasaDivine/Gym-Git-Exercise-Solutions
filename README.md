# Gym-Git-Exercise-Solutions
This is a repository for git exercises.


BUNDLE 1

EXERCISE 1
PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git branch
* main
PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git branch -m
fatal: branch name required
PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git checkout main
M       README.md
Already on 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git branch -m master
PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git branch
* master
PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git add .
PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git commit -m "Renaming my branch"
[master 63f55bc] Renaming my branch
 1 file changed, 2 insertions(+), 1 deletion(-)
PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git push

    git push origin HEAD:main

To push to the branch of the same name on the remote, use

    git push origin HEAD

To choose either option permanently, see push.default in 'git help config'.

To avoid automatically configuring an upstream branch when its name
won't match the local branch, see option 'simple' of branch.autoSetupMerge
in 'git help config'.

PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git push origin HEAD
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 318 bytes | 318.00 KiB/s, done.    
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)   
remote:
remote: Create a pull request for 'master' on GitHub by visiting:
remote:      https://github.com/BirasaDivine/Gym-Git-Exercise-Solutions/pull/new/master
-b master
fatal: a branch named 'master' already exists
PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git checkout -b dev
Switched to a new branch 'dev'
PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git status
On branch dev
nothing to commit, working tree clean
PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git branch test
PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git status
On branch dev
nothing to commit, working tree clean
PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git branch -d test
Deleted branch test (was 63f55bc).

EXERCISE 2