# Gym-Git-Exercise-Solutions
This is a repository for git exercises.


# BUNDLE 1

# EXERCISE 1
```bash
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
```
# EXERCISE 2
```bash
PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git add .\home.html
PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git stash push -m "home.html"
Saved working directory and index state On main: home.html      
PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git add .\about.html
PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git stash push -m "About HTML"
Saved working directory and index state On main: About HTML
PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git add .\team.html
PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git stash push -m "Team HTML"
Saved working directory and index state On main: Team HTML
PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git status
On branch main
nothing to commit, working tree clean
PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git stash pop

On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped refs/stash@{0} (cf05c726123ecc30b44181ff580b87052c89161e)
PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git stash push -m "Team HTML"
Saved working directory and index state On main: Team HTML
PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git stash list
stash@{0}: On main: Team HTML
stash@{1}: On main: About HTML
stash@{2}: On main: home.html
PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git stash pop stash@{1}
error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]

    -q, --[no-]quiet      be quiet, only report errors
    --[no-]index          attempt to recreate the index

PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git stash pop stash@{1}
error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]

    -q, --[no-]quiet      be quiet, only report errors
    --[no-]index          attempt to recreate the index

PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git stash pop stash@{1}
error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]
stash@{0}: On main: Team HTML
stash@{1}: On main: About HTML
stash@{2}: On main: home.html
PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions> git stash pop stash@{1}
error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]

    -q, --[no-]quiet      be quiet, only report errors
    --[no-]index          attempt to recreate the index

PS C:\Users\LENOVO\ALU\Gym-Git-Exercise-Solutions>
LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git stash list
stash@{0}: On main: Team HTML
stash@{1}: On main: About HTML
bash: gi: command not found

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solubash: gi: command not found

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git stash pop stash@{0}
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)       
        new file:   team.html

Dropped stash@{0} (b90659d1a2948e1f19d398bb64bfd2ec51d7d27d)

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git stash push -m "Team HTML"
Saved working directory and index state On main: Team HTML

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git stash list
stash@{0}: On main: Team HTML
stash@{1}: On main: About HTML
stash@{2}: On main: home.html

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git stash pop stash@{1}
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)       
        new file:   about.html

Dropped stash@{1} (c854079c9ee2ed2fbc3ca87f45228d5acc36ca5f)

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git stash pop stash@{2}
fatal: log for 'stash' only has 2 entries

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git add .

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git commit -m "Exercise 2"
LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git push -u origin main
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 313 bytes | 313.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/BirasaDivine/Gym-Git-Exercise-Solutions.git
   3c09305..c29ffbc  main -> main
branch 'main' set up to track 'origin/main'.

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git branch 
  checkout
  dev
* main
  master

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git branch checkout dev
fatal: a branch named 'checkout' already exists

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git branch dev
fatal: a branch named 'dev' already exists

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git checkout dev
Switched to branch 'dev'

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (dev)
$ git checkout master
Switched to branch 'master'
Your branch is behind 'origin/main' by 1 commit, and can be fast-forwarded.
  (use "git pull" to update your local branch)

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (master)
$ git checkout dev
Switched to branch 'dev'

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (dev)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git checkout checkout
Switched to branch 'checkout'

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (checkout)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git stash pop stash@{0}
On branch main
Your branch is up to date with 'origin/main'.

  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Dropped stash@{0} (b21850c7d04a9380c8cc023394faf8c82dea9b3b)

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git stash list
stash@{0}: On main: home.html

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ it stash list
bash: it: command not found

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git stash list
stash@{0}: On main: home.html

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git stash push -m "Team HTML"
Saved working directory and index state On main: Team HTML

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git stash list
stash@{0}: On main: Team HTML
stash@{1}: On main: home.html

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git stast pop stash@{1}
git: 'stast' is not a git command. See 'git --help'.

The most similar command is
        stash

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git stash pop stash@{1}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Dropped stash@{1} (d22b4bd5d1d47d0e2e07b6152dd2c424ff764693)

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git stash list
stash@{0}: On main: Team HTML

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git add .

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git commit -m "Push pop about and home"
[main 7e75816] Push pop about and home
 2 files changed, 84 insertions(+), 1 deletion(-)
 create mode 100644 home.html

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git stash list
stash@{0}: On main: Team HTML

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git stash pop 
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

        new file:   team.html

Unmerged paths:
  (use "git restore --staged <file>..." to unstage)
  (use "git add <file>..." to mark resolution)
        both modified:   README.md

The stash entry is kept in case you need it again.

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git reset --hard
HEAD is now at 7e75816 Push pop about and home
```
 # BUNDLE 2
 # EXERCISE 1
 ```bash
 remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/BirasaDivine/Gym-Git-Exercise-Solutions/pull/new/ft/bundle-2
remote:
To https://github.com/BirasaDivine/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git status
On branch ft/bundle-2
Your branch is up to date with 'origin/ft/bundle-2'.      

nothing to commit, working tree clean
```
# EXERCISE 2
```bash
LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git checkout main
Switched to branch 'main'
Your branch is behind 'origin/main' by 2 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git staus
git: 'staus' is not a git command. See 'git --help'.

The most similar command is
        status

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git status
On branch main
Your branch is behind 'origin/main' by 2 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)

nothing to commit, working tree clean

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git pull
Updating e723e28..3832b1c
Fast-forward
 services.html | 14 ++++++++++++++
 1 file changed, 14 insertions(+)
 create mode 100644 services.html

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git btanch ft/service-redesign
git: 'btanch' is not a git command. See 'git --help'.

The most similar command is
        branch

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git branch ft/service-redesign

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git add .

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git commit -m "Changes on Service html"
[ft/service-redesign f816068] Changes on Service html
 1 file changed, 1 insertion(+), 1 deletion(-)

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign    

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ ft/service-redesign
bash: ft/service-redesign: No such file or directory

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git push --set-upstream origin ft/service-redesign
al objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/BirasaDivine/Gym-Git-Exercise-Solutions/pull/new/ft/service-redesign
al objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/BirasaDivine/Gym-Git-Exercise-Solutions/pull/new/ft/service-redesign
remote:
To https://github.com/BirasaDivine/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git add .

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git commit -m "Service html on main"
[main ce0ae36] Service html on main
 1 file changed, 1 insertion(+), 1 deletion(-)

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 331 bytes | 331.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/BirasaDivine/Gym-Git-Exercise-Solutions.git
   3832b1c..ce0ae36  main -> main

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git diff ft/service-redesign..main
diff --git a/services.html b/services.html
index b710bf6..807a519 100644
--- a/services.html
+++ b/services.html
@@ -8,7 +8,7 @@
 </head>
+    <p> Git Exercises</p>
 </body>

 </html>
\ No newline at end of file

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git merge main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign|MERGING)
$ git status
On branch ft/service-redesign
Your branch is up to date with 'origin/ft/service-redesign'.

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign|MERGING)
$ git add .

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign|MERGING)
$ git commit -m "Merged the conflicts"
[ft/service-redesign 4f1d1c3] Merged the conflicts

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git push
Enumerating objects: 1, done.
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 225 bytes | 225.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/BirasaDivine/Gym-Git-Exercise-Solutions.git
   f816068..4f1d1c3  ft/service-redesign -> ft/service-redesign
   ```
# BUNDLE 3

# EXERCISE 1
```bash
LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git branch ft/team-page

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git add team.html 

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git add .

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git commit -m "Team HTML"
[ft/service-redesign 94259ee] Team HTML
 1 file changed, 14 insertions(+)
 create mode 100644 team.html

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 429 bytes | 143.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/BirasaDivine/Gym-Git-Exercise-Solutions.git
   4f1d1c3..94259ee  ft/service-redesign -> ft/service-redesign

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git branch ft/contact-page

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'

commit 4f1d1c3c1431143a936da4f9f01b69b0dd824517 (HEAD -> ft/team-page)
commit 4f1d1c3c1431143a936da4f9f01b69b0dd824517 (HEAD -> ft/team-page)
Merge: f816068 ce0ae36
Author: Birasa Divine <b.divine@alustudent.com>
Date:   Tue Dec 17 12:07:22 2024 +0200

    Merged the conflicts

commit ce0ae3662820aee9bb765c64b32867a7f485314b (origin/main, origin/HEAD, main, ft/contact-page)
Author: Birasa Divine <b.divine@alustudent.com>
Date:   Tue Dec 17 11:50:02 2024 +0200

    Service html on main

commit f816068166ca278bc9a3f44d55d3fff79340761c
Author: Birasa Divine <b.divine@alustudent.com>
Date:   Tue Dec 17 11:44:40 2024 +0200

    Changes on Service html

commit 3832b1ca705fea8aec47ec54fb019e313d089631
Merge: e723e28 784e44d
Author: Ian Ganza <144003894+i-ganza007@users.noreply.github.com>
Date:   Tue Dec 17 11:24:48 2024 +0200

    Merge pull request #1 from BirasaDivine/ft/bundle-2   

    Services HTML

Date:   Tue Dec 17 10:16:51 2024 +0200

    Exercise 2

commit 63f55bcb3cbba6733b68f46c1acd94689184578d (origin/master, master, dev, checkout)
Author: Birasa Divine <b.divine@alustudent.com>
Date:   Mon Dec 16 13:14:05 2024 +0200

    Renaming my branch

commit 3c09305365152cf12d11c2db60b43628f13954b2
Author: Birasa Divine <b.divine@alustudent.com>
Date:   Mon Dec 16 10:52:01 2024 +0200

    Initial commit
~
...skipping...
Date:   Tue Dec 17 10:16:51 2024 +0200

    Exercise 2

commit 63f55bcb3cbba6733b68f46c1acd94689184578d (origin/master, master, dev, checkout)
Author: Birasa Divine <b.divine@alustudent.com>
Date:   Mon Dec 16 13:14:05 2024 +0200

    Renaming my branch

commit 3c09305365152cf12d11c2db60b43628f13954b2
Author: Birasa Divine <b.divine@alustudent.com>
Date:   Mon Dec 16 10:52:01 2024 +0200

    Initial commit
~
...skipping...
Date:   Tue Dec 17 10:16:51 2024 +0200

    Exercise 2

commit 63f55bcb3cbba6733b68f46c1acd94689184578d (origin/master, master, dev, checkout)
Author: Birasa Divine <b.divine@alustudent.com>
Date:   Mon Dec 16 13:14:05 2024 +0200

Date:   Mon Dec 16 10:52:01 2024 +0200

~

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/team-page)
$ git checkout ft/contact-page
M       README.md
Switched to branch 'ft/contact-page'

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git checkout ft/team-page
M       README.md
Switched to branch 'ft/team-page'

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/team-page)
$ git checkout ft/service-redesign
M       README.md
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git log
commit 94259eeaf45516f24bfa46d57f012cecaaf2dd19 (HEAD -> ft/service-redesign, origin/ft/service-redesign)
Author: Birasa Divine <b.divine@alustudent.com>
Date:   Tue Dec 17 12:20:25 2024 +0200

    Team HTML

commit 4f1d1c3c1431143a936da4f9f01b69b0dd824517 (ft/team-page)
Merge: f816068 ce0ae36
Author: Birasa Divine <b.divine@alustudent.com>
Date:   Tue Dec 17 12:07:22 2024 +0200

    Merged the conflicts

commit ce0ae3662820aee9bb765c64b32867a7f485314b (origin/main, origin/HEAD, master, main, ft/contact-page)
Author: Birasa Divine <b.divine@alustudent.com>
Date:   Tue Dec 17 11:50:02 2024 +0200

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git checkout ft/team-page
M       README.md
Switched to branch 'ft/team-page'

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/team-page)
$ git cherry-pick 94259eeaf45516f24bfa46d57f012cecaaf2dd19
[ft/team-page 1d818cb] Team HTML
 Date: Tue Dec 17 12:20:25 2024 +0200
 1 file changed, 14 insertions(+)
 create mode 100644 team.html

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/team-page)
$ git checkout ft/
ft/bundle-2           ft/contact-page       ft/service-redesign   ft/team-page

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/team-page)
$ git checkout ft/
ft/bundle-2           ft/contact-page       ft/service-redesign   ft/team-page

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/team-page)
$ git checkout ft/
ft/bundle-2           ft/contact-page       ft/service-redesign   ft/team-page

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/team-page)
$ git checkout ft/service-redesign 
M       README.md
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git log
commit 94259eeaf45516f24bfa46d57f012cecaaf2dd19 (HEAD -> ft/service-redesign, origin/ft/service-redesign)
Author: Birasa Divine <b.divine@alustudent.com>
Date:   Tue Dec 17 12:20:25 2024 +0200

    Team HTML

commit 4f1d1c3c1431143a936da4f9f01b69b0dd824517
Merge: f816068 ce0ae36
Author: Birasa Divine <b.divine@alustudent.com>
Date:   Tue Dec 17 12:07:22 2024 +0200

    Merged the conflicts

commit ce0ae3662820aee9bb765c64b32867a7f485314b (origin/main, origin/HEAD, master, main, ft/contact-page)
Author: Birasa Divine <b.divine@alustudent.com>
Date:   Tue Dec 17 11:50:02 2024 +0200

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git rebase 4f1d1c3c1431143a936da4f9f01b69b0dd824517~
error: cannot rebase: You have unstaged changes.
error: Please commit or stash them.

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git add .

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git stash
Saved working directory and index state WIP on ft/service-redesign: 94259ee Team HTML

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git rebase 4f1d1c3c1431143a936da4f9f01b69b0dd824517~
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
error: could not apply ce0ae36... Service html on main
hint: Resolve all conflicts manually, mark them as resolved with
hint: "git add/rm <conflicted_files>", then run "git rebase --continue".
hint: You can instead skip this commit: run "git rebase --skip".
hint: To abort and get back to the state before "git rebase", run "git rebase --abort".
hint: Disable this message with "git config advice.mergeConflict false"
Could not apply ce0ae36... Service html on main

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign|REBASE 1/2)
$ git rebase --abort

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git rebase -i 4f1d1c3c1431143a936da4f9f01b69b0dd824517~
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
error: could not apply ce0ae36... Service html on main
hint: Resolve all conflicts manually, mark them as resolved with
hint: "git add/rm <conflicted_files>", then run "git rebase --continue".
hint: You can instead skip this commit: run "git rebase --skip".
hint: To abort and get back to the state before "git rebase", run "git rebase --abort".
hint: Disable this message with "git config advice.mergeConflict false"
Could not apply ce0ae36... Service html on main

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign|REBASE 1/2)
$ git log
commit f816068166ca278bc9a3f44d55d3fff79340761c (HEAD)
Author: Birasa Divine <b.divine@alustudent.com>
Date:   Tue Dec 17 11:44:40 2024 +0200

    Changes on Service html

commit 3832b1ca705fea8aec47ec54fb019e313d089631
Merge: e723e28 784e44d
Author: Ian Ganza <144003894+i-ganza007@users.noreply.github.com>
Date:   Tue Dec 17 11:24:48 2024 +0200

    Merge pull request #1 from BirasaDivine/ft/bundle-2

    Services HTML

commit 784e44dacf02e8d906640f5a892884420277833d (origin/ft/bundle-2, ft/bundle-2)
Author: Birasa Divine <b.divine@alustudent.com>
Date:   Tue Dec 17 11:19:34 2024 +0200

    Services HTML

commit e723e2883cb4c26651076a862d3ec6968178a989
Author: Birasa Divine <b.divine@alustudent.com>
Date:   Tue Dec 17 10:43:34 2024 +0200

    Exercise 2

commit 7e75816609628b52918c91bdbdddd75986545803
Author: Birasa Divine <b.divine@alustudent.com>
Date:   Tue Dec 17 10:34:02 2024 +0200

commit f816068166ca278bc9a3f44d55d3fff79340761c (HEAD)
Author: Birasa Divine <b.divine@alustudent.com>
Date:   Tue Dec 17 11:44:40 2024 +0200

    Changes on Service html

commit 3832b1ca705fea8aec47ec54fb019e313d089631
Merge: e723e28 784e44d
Author: Ian Ganza <144003894+i-ganza007@users.noreply.github.com>
Date:   Tue Dec 17 11:24:48 2024 +0200

    Merge pull request #1 from BirasaDivine/ft/bundle-2

    Services HTML

commit 784e44dacf02e8d906640f5a892884420277833d (origin/ft/bundle-2, ft/bundle-2)
Author: Birasa Divine <b.divine@alustudent.com>

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign|REBASE 1/2)
$ git rebase --abort 

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git log
commit 94259eeaf45516f24bfa46d57f012cecaaf2dd19 (HEAD -> ft/service-redesign, origin/ft/service-redesign)
Author: Birasa Divine <b.divine@alustudent.com>
Date:   Tue Dec 17 12:20:25 2024 +0200

    Team HTML

commit 4f1d1c3c1431143a936da4f9f01b69b0dd824517
Merge: f816068 ce0ae36
Author: Birasa Divine <b.divine@alustudent.com>
Date:   Tue Dec 17 12:07:22 2024 +0200

    Merged the conflicts

commit ce0ae3662820aee9bb765c64b32867a7f485314b (origin/main, origin/HEAD, master, main, ft/contact-page)
Author: Birasa Divine <b.divine@alustudent.com>
Date:   Tue Dec 17 11:50:02 2024 +0200

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git rebase --abort
fatal: no rebase in progress

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git log
commit 94259eeaf45516f24bfa46d57f012cecaaf2dd19 (HEAD -> ft/service-redesign, origin/ft/service-redesign)
Author: Birasa Divine <b.divine@alustudent.com>
Date:   Tue Dec 17 12:20:25 2024 +0200

    Team HTML

commit 4f1d1c3c1431143a936da4f9f01b69b0dd824517
Merge: f816068 ce0ae36
Author: Birasa Divine <b.divine@alustudent.com>
Date:   Tue Dec 17 12:07:22 2024 +0200

    Merged the conflicts

commit ce0ae3662820aee9bb765c64b32867a7f485314b (origin/main, origin/HEAD, master, main, ft/contact-page)
Author: Birasa Divine <b.divine@alustudent.com>
Date:   Tue Dec 17 11:50:02 2024 +0200

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git rebase -i 4f1d1c3c1431143a936da4f9f01b69b0dd824517~
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
error: could not apply ce0ae36... Service html on main
hint: Resolve all conflicts manually, mark them as resolved with
hint: "git add/rm <conflicted_files>", then run "git rebase --continue".
hint: You can instead skip this commit: run "git rebase --skip".
hint: To abort and get back to the state before "git rebase", run "git rebase --abort".
hint: Disable this message with "git config advice.mergeConflict false"
Could not apply ce0ae36... Service html on main

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign|REBASE 1/2)
$ git rebase --abort

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/team-page)
$ git add .

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/team-page)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/team-page)
$ git add .

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/team-page)
$ git commit -m "Team HTML"
On branch ft/team-page
nothing to commit, working tree clean

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/team-page)
$ git push
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/team-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/team-page)
$ git push --set-upstream origin ft/team-page
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/BirasaDivine/Gym-Git-Exercremote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/BirasaDivine/Gym-Git-Exercise-Solutions/pull/new/ft/team-page
remote:
To https://github.com/BirasaDivine/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git branch ft/contact-page
fatal: a branch named 'ft/contact-page' already exists

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (main)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.     

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/team-page)
$ git log
commit 1d818cb73ff41b7754bfb1122d3b153fc3717173 (HEAD -> ft/team-page, origin/ft/team-page)
Author: Birasa Divine <b.divine@alustudent.com>
Date:   Tue Dec 17 12:20:25 2024 +0200

    Team HTML

commit 4f1d1c3c1431143a936da4f9f01b69b0dd824517
Merge: f816068 ce0ae36
Author: Birasa Divine <b.divine@alustudent.com>
Date:   Tue Dec 17 12:07:22 2024 +0200

    Merged the conflicts

commit ce0ae3662820aee9bb765c64b32867a7f485314b (origin/main, origin/HEAD, master, main, ft/contact-page)

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git cherry-pick
usage: git cherry-pick [--edit] [-n] [-m <parent-number>] [-s] [-x] [--ff]
                       [-S[<keyid>]] <commit>...
   or: git cherry-pick (--continue | --skip | --abort | --quit)

    --quit                end revert or cherry-pick sequence
    --continue            resume revert or cherry-pick sequence
    --abort               cancel revert or cherry-pick sequence
    --skip                skip current commit and continue
    --[no-]cleanup <mode> how to strip spaces and #comments from message
    -n, --no-commit       don't automatically commit      
    --commit              opposite of --no-commit
    -e, --[no-]edit       edit the commit message
    -s, --[no-]signoff    add a Signed-off-by trailer     
    -m, --[no-]mainline <parent-number>
                          select mainline parent
    --[no-]rerere-autoupdate
                          update the index with reused conflict resolution if possible
    --[no-]strategy <strategy>
                          merge strategy
    -X, --[no-]strategy-option <option>
                          option for merge strategy       
    -S, --[no-]gpg-sign[=<key-id>]
                          GPG sign commit
    -x                    append commit name
    --[no-]ff             allow fast-forward
    --[no-]allow-empty    preserve initially empty commits
tead
    --empty (stop|drop|keep)
                          how to handle commits that become empty
tead
    --empty (stop|drop|keep)
                          how to handle commits that become empty


LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git cherry-pick 1d818cb73ff41b7754bfb1122d3b153fc3717173[ft/contact-page 0c1116f] Team HTML
 Date: Tue Dec 17 12:20:25 2024 +0200
 1 file changed, 14 insertions(+)
 create mode 100644 team.html

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git add .

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git commit -m "Creating Contact Page"
[ft/contact-page 7199b31] Creating Contact Page
 1 file changed, 14 insertions(+)
 create mode 100644 contact.html

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git push
fatal: The current branch ft/contact-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/contact-page        

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git push --set-upstream origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 686 bytes | 686.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/BirasaDivine/Gym-Git-Exercise-Solutions/pull/new/ft/contact-page
remote:
To https://github.com/BirasaDivine/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/contact-page -> ft/contact-page   
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git branch -b ft/faq-page
error: unknown switch `b'
usage: git branch [<options>] [-r | -a] [--merged] [--no-merged]
   or: git branch [<options>] [-f] [--recurse-submodules] <branch-name> [<start-point>]
   or: git branch [<options>] [-l] [<pattern>...]
   or: git branch [<options>] [-r] (-d | -D) <branch-name>...
   or: git branch [<options>] (-m | -M) [<old-branch>] <new-branch>
   or: git branch [<options>] (-c | -C) [<old-branch>] <new-branch>
   or: git branch [<options>] [-r | -a] [--points-at]     
   or: git branch [<options>] [-r | -a] [--format]        

Generic options
    -v, --[no-]verbose    show hash and subject, give twice for upstream branch
    -q, --[no-]quiet      suppress informational messages 
    -t, --[no-]track[=(direct|inherit)]
                          set branch tracking configuration
    -u, --[no-]set-upstream-to <upstream>
                          change the upstream info        
    --[no-]unset-upstream unset the upstream info
    --[no-]color[=<when>] use colored output
    -r, --remotes         act on remote-tracking branches 
    --contains <commit>   print only branches that contain the commit
    --no-contains <commit>
                          print only branches that don't contain the commit
    --[no-]abbrev[=<n>]   use <n> digits to display object names

Specific git-branch actions:
    -a, --all             list both remote-tracking and local branches
    -d, --[no-]delete     delete fully merged branch      
    -D                    delete branch (even if not merged)
    -m, --[no-]move       move/rename a branch and its reflog
    -M                    move/rename a branch, even if target exists
    --[no-]omit-empty     do not output a newline after empty formatted refs
    -c, --[no-]copy       copy a branch and its reflog    
    -C                    copy a branch, even if target exists
    -l, --[no-]list       list branch names
    --[no-]show-current   show current branch name        
    --[no-]create-reflog  create the branch's reflog      
    --[no-]edit-description
                          edit the description for the branch
    -f, --[no-]force      force creation, move/rename, deletion
    --merged <commit>     print only branches that are merged
    --no-merged <commit>  print only branches that are not merged
    --[no-]column[=<style>]
                          list branches in columns        
    --[no-]sort <key>     field name to sort on
    --[no-]points-at <object>
                          print only branches of the object
    -i, --[no-]ignore-case
                          sorting and filtering are case insensitive
    --[no-]recurse-submodules
                          recurse through submodules      
    --[no-]format <format>
                          format to use for the output    


LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git branch ft/faq-page

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git checkout ft/faq-page
Switched to branch 'ft/faq-page'

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git add .

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git commit -m "FAQ HTML"
[ft/faq-page 95820a3] FAQ HTML
 1 file changed, 14 insertions(+)
 create mode 100644 faq.html

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git push
fatal: The current branch ft/faq-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/faq-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/BirasaDivine/Gym-Git-Exercise-Solutions/pull/new/ft/faq-page
remote:
To https://github.com/BirasaDivine/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.
LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git revert 1d818cb73ff41b7754bfb1122d3b153fc3717173
[ft/faq-page 16b34b2] Revert "Team HTML"
 1 file changed, 14 deletions(-)
 delete mode 100644 team.html

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git add .

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git commit -m "Revert TEAM HTML"
On branch ft/faq-page
Your branch is ahead of 'origin/ft/faq-page' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

LENOVO@DESKTOP-G7D6FUR MINGW64 ~/ALU/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 276 bytes | 276.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/BirasaDivine/Gym-Git-Exercise-Solutions.git
   95820a3..16b34b2  ft/faq-page -> ft/faq-page
```
# EXERCISE 2