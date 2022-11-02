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
