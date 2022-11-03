# Thegym Git Exercise Solutions

## Bundle 1

### Exercise 1

```bash
➜  bundle-1 git init
Initialized empty Git repository in /home/jacob-dev/exercices/Git/bundle-1/.git/
➜  bundle-1 git:(main) git branch -m master main
error: refname refs/heads/master not found
fatal: Branch rename failed
➜  bundle-1 git:(main) echo hello-world.txt > "Hello World"
➜  bundle-1 git:(main) ✗ gh repo create                             
? What would you like to do? Push an existing local repository to GitHub
? Path to local repository .
? Repository name thegym-git-exercise-bundle-1
? Description Thegym git exercise bundle 1
? Visibility Public
✓ Created repository jacob-js/thegym-git-exercise-bundle-1 on GitHub
? Add a remote? Yes
? What should the new remote be called? origin
✓ Added remote https://github.com/jacob-js/thegym-git-exercise-bundle-1.git
➜  bundle-1 git:(main) ✗ git add .
➜  bundle-1 git:(main) ✗ git commit -m 'first commit'
[main (root-commit) 9e677e7] first commit
 1 file changed, 1 insertion(+)
 create mode 100644 Hello World
➜  bundle-1 git:(main) git push --set-upstream origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 232 bytes | 116.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/jacob-js/thegym-git-exercise-bundle-1.git
 * [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
➜  bundle-1 git:(main) git checkout -b dev
Switched to a new branch 'dev'
➜  bundle-1 git:(dev) git checkout -b test
Switched to a new branch 'test'
➜  bundle-1 git:(test) git checkout dev
Switched to branch 'dev'
➜  bundle-1 git:(dev) git branch test -d
Deleted branch test (was 9e677e7).
```

### Exercise 2

```bash
➜  bundle-1 git:(dev) ✗ touch home.html
➜  bundle-1 git:(dev) ✗ git stash -u 
Saved working directory and index state WIP on dev: 9e677e7 first commit
➜  bundle-1 git:(dev) touch about.html
➜  bundle-1 git:(dev) ✗ git stash -u    
Saved working directory and index state WIP on dev: 9e677e7 first commit
➜  bundle-1 git:(dev) touch team.html 
➜  bundle-1 git:(dev) ✗ git stash -u   
Saved working directory and index state WIP on dev: 9e677e7 first commit
➜  bundle-1 git:(dev) git stash pop stash@{1}
Already up to date.
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html

nothing added to commit but untracked files present (use "git add" to track)
Dropped stash@{1} (1665f48b0fea4ad791ef0c0474ace26cb4352453)
➜  bundle-1 git:(dev) ✗ git stash pop stash@{1}
Already up to date.
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html
        home.html

nothing added to commit but untracked files present (use "git add" to track)
Dropped stash@{1} (3a57879d3d7828ca5d8fd4e14732065411523aed)
➜  bundle-1 git:(dev) ✗ git add .
➜  bundle-1 git:(dev) ✗ git commit -m 'add files'
[dev 3b4af54] add files
 2 files changed, 12 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
➜  bundle-1 git:(dev) ✗ git commit -am 'add files'
[dev 15e609e] add files
 1 file changed, 12 insertions(+)
➜  bundle-1 git:(dev) git push origin dev       
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (6/6), 736 bytes | 184.00 KiB/s, done.
Total 6 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/jacob-js/thegym-git-exercise-bundle-1/pull/new/dev
remote: 
To https://github.com/jacob-js/thegym-git-exercise-bundle-1.git
 * [new branch]      dev -> dev
➜  bundle-1 git:(dev) git stash pop stash@{0}   
Already up to date.
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)
Dropped stash@{0} (5a87ea9a6687e5df9448a9a18b81659a35352001)
➜  bundle-1 git:(dev) ✗ git reset --hard
HEAD is now at 15e609e add files
➜  bundle-1 git:(dev) ✗ git clean -f
Removing team.html
```
