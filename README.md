kuzia@Sokolovskaya13 MINGW64 ~/OneDrive/Рабочий стол/git-homeworks-neuro-merge (main)
$ git checkout -b fix
Switched to a new branch 'fix'

kuzia@Sokolovskaya13 MINGW64 ~/OneDrive/Рабочий стол/git-homeworks-neuro-merge (fix)
$ git status
On branch fix
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

no changes added to commit (use "git add" and/or "git commit -a")

kuzia@Sokolovskaya13 MINGW64 ~/OneDrive/Рабочий стол/git-homeworks-neuro-merge (fix)
$ git add -A

kuzia@Sokolovskaya13 MINGW64 ~/OneDrive/Рабочий стол/git-homeworks-neuro-merge (fix)
$ git commit -m "Changed1"
[fix 291cb8f] Changed1
 1 file changed, 2 insertions(+)

kuzia@Sokolovskaya13 MINGW64 ~/OneDrive/Рабочий стол/git-homeworks-neuro-merge (fix)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

kuzia@Sokolovskaya13 MINGW64 ~/OneDrive/Рабочий стол/git-homeworks-neuro-merge (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

no changes added to commit (use "git add" and/or "git commit -a")

kuzia@Sokolovskaya13 MINGW64 ~/OneDrive/Рабочий стол/git-homeworks-neuro-merge (main)
$ git commit -a -m "Changed2"
[main 0ad088d] Changed2
 1 file changed, 1 insertion(+)

kuzia@Sokolovskaya13 MINGW64 ~/OneDrive/Рабочий стол/git-homeworks-neuro-merge (main)
$ git merge fix
Auto-merging index.html
CONFLICT (content): Merge conflict in index.html
Automatic merge failed; fix conflicts and then commit the result.

kuzia@Sokolovskaya13 MINGW64 ~/OneDrive/Рабочий стол/git-homeworks-neuro-merge (main|MERGING)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   index.html

no changes added to commit (use "git add" and/or "git commit -a")

kuzia@Sokolovskaya13 MINGW64 ~/OneDrive/Рабочий стол/git-homeworks-neuro-merge (main|MERGING)
$ git commit -a -m "Conflict resolved"
[main ff5efea] Conflict resolved


2.

kuzia@Sokolovskaya13 MINGW64 ~/OneDrive/Рабочий стол/git-homeworks-neuro-merge (main)
$ git remote remove origin
error: could not delete references: cannot lock ref 'refs/remotes/origin/main': Unable to create 'C:/Users/kuzia/OneDrive/Рабочий стол/git-homeworks-neuro-merge/.git/refs/remotes/origin/main.lock': File exists.

Another git process seems to be running in this repository, or the lock file maybe stale

kuzia@Sokolovskaya13 MINGW64 ~/OneDrive/Рабочий стол/git-homeworks-neuro-merge (main)
$ git remote -v
origin  git@github.com:Kris-1303/git-homeworks-neuro-merge.git (fetch)
origin  git@github.com:Kris-1303/git-homeworks-neuro-merge.git (push)

kuzia@Sokolovskaya13 MINGW64 ~/OneDrive/Рабочий стол/git-homeworks-neuro-merge (main)
$ git remote set-url origin git@github.com:Kris-1303/Conflict.git

kuzia@Sokolovskaya13 MINGW64 ~/OneDrive/Рабочий стол/git-homeworks-neuro-merge (main)
$ git remote -v
origin  git@github.com:Kris-1303/Conflict.git (fetch)
origin  git@github.com:Kris-1303/Conflict.git (push)