# Gym-Git-Exercise-Solutions
This is a repository for git exercises.


# BUNDLE 1

# EXERCISE 1
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

# EXERCISE 2
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