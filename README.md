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

## Bundle 2

### Exercise 2


```bash
➜  bundle-1 git:(ft/bundle-2) git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
➜  bundle-1 git:(main) git pull
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 617 bytes | 154.00 KiB/s, done.
From https://github.com/jacob-js/thegym-git-exercise-bundle-1
   9e677e7..b431d0f  main       -> origin/main
Updating 9e677e7..b431d0f
Fast-forward
 about.html    | 12 ++++++++++++
 home.html     | 12 ++++++++++++
 services.html | 12 ++++++++++++
 3 files changed, 36 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 services.html
➜  bundle-1 git:(main) git commit -am 'update services page'
[main 72d05c4] update services page
 1 file changed, 1 insertion(+), 1 deletion(-)
➜  bundle-1 git:(main) git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), 
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 323 bytes | 107.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/jacob-js/thegym-git-exercise-bundle-1.git
   b431d0f..72d05c4  main -> main
➜  bundle-1 git:(main) git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'
➜  bundle-1 git:(ft/service-redesign) git commit -am 'update services page'
[ft/service-redesign 7799202] update services page
 1 file changed, 1 insertion(+), 1 deletion(-)
➜  bundle-1 git:(ft/service-redesign) git push origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 287 bytes | 95.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: 
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/jacob-js/thegym-git-exercise-bundle-1/pull/new/ft/service-redesign
remote: 
To https://github.com/jacob-js/thegym-git-exercise-bundle-1.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
➜  bundle-1 git:(ft/service-redesign) git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
➜  bundle-1 git:(main) git commit -am 'add new flag'
[main ebbcbb9] add new flag
 1 file changed, 1 insertion(+), 1 deletion(-)
➜  bundle-1 git:(main) git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 313 bytes | 156.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/jacob-js/thegym-git-exercise-bundle-1.git
   72d05c4..ebbcbb9  main -> main
➜  bundle-1 git:(main) git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
➜  bundle-1 git:(ft/service-redesign) git diff main ft/service-redesign
diff --git a/services.html b/services.html
index 95ff7f6..c5e6724 100644
--- a/services.html
+++ b/services.html
@@ -7,6 +7,6 @@
     <title>Document</title>
 </head>
 <body>
-    <h1>Our Services <span>New</span></h1>
+    <h1>Services</h1>
 </body>
 </html>
\ No newline at end of file
➜  bundle-1 git:(ft/service-redesign) git merge  main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.
➜  bundle-1 git:(ft/service-redesign) ✗ git commit -am 'merge with main branch'
[ft/service-redesign 79984ad] merge with main branch
➜  bundle-1 git:(ft/service-redesign) git push origin ft/service-redesign
Enumerating objects: 1, done.
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 220 bytes | 220.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/jacob-js/thegym-git-exercise-bundle-1.git
   7799202..79984ad  ft/service-redesign -> ft/service-redesign
```

## Bundle 3

## Exercise 1

```bash
➜  bundle-1 git:(ft/service-redesign) git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'
➜  bundle-1 git:(ft/team-page) git add .
➜  bundle-1 git:(ft/team-page) ✗ git commit -m 'add team page'
[ft/team-page 9b5b7f8] add team page
 1 file changed, 12 insertions(+)
 create mode 100644 team.html
➜  bundle-1 git:(ft/team-page) git push
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/team-page

➜  bundle-1 git:(ft/team-page) git push origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 449 bytes | 449.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/jacob-js/thegym-git-exercise-bundle-1/pull/new/ft/team-page
remote: 
To https://github.com/jacob-js/thegym-git-exercise-bundle-1.git
 * [new branch]      ft/team-page -> ft/team-page
➜  bundle-1 git:(ft/team-page) git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
➜  bundle-1 git:(main) git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'
➜  bundle-1 git:(ft/contact-page) git checkout ft/team-page
Switched to branch 'ft/team-page'
➜  bundle-1 git:(ft/team-page) git log
➜  bundle-1 git:(ft/team-page) git checkout ft/contact-page
Switched to branch 'ft/contact-page'
➜  bundle-1 git:(ft/contact-page) git show
➜  bundle-1 git:(ft/contact-page) git cherry-pick 9b5b7f82a7ffc11075a9d39df9e4e6cce293404a
[ft/contact-page a273931] add team page
 Date: Wed Nov 9 11:25:30 2022 +0200
 1 file changed, 12 insertions(+)
 create mode 100644 team.html
➜  bundle-1 git:(ft/contact-page) git add .
➜  bundle-1 git:(ft/contact-page) ✗ git commit -m 'add contact page'
[ft/contact-page 1962dfe] add contact page
 1 file changed, 12 insertions(+)
 create mode 100644 contact.html
➜  bundle-1 git:(ft/contact-page) git push origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 689 bytes | 689.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/jacob-js/thegym-git-exercise-bundle-1/pull/new/ft/contact-page
remote: 
To https://github.com/jacob-js/thegym-git-exercise-bundle-1.git
 * [new branch]      ft/contact-page -> ft/contact-page
 ➜  bundle-1 git:(ft/contact-page) git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'
➜  bundle-1 git:(ft/faq-page) git add .
➜  bundle-1 git:(ft/faq-page) ✗ git commit -m 'create faq page'
[ft/faq-page 874f998] create faq page
 1 file changed, 12 insertions(+)
 create mode 100644 faq.html
➜  bundle-1 git:(ft/faq-page) git push origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 440 bytes | 440.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/jacob-js/thegym-git-exercise-bundle-1/pull/new/ft/faq-page
remote: 
To https://github.com/jacob-js/thegym-git-exercise-bundle-1.git
 * [new branch]      ft/faq-page -> ft/faq-page
➜  bundle-1 git:(ft/faq-page) git revert 9b5b7f82a7ffc11075a9d39df9e4e6cce293404a
[ft/faq-page 0bca3fa] Revert "add team page"
 1 file changed, 12 deletions(-)
 delete mode 100644 team.html
➜  bundle-1 git:(ft/faq-page) git push origin ft/faq-page
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 268 bytes | 268.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/jacob-js/thegym-git-exercise-bundle-1.git
   874f998..0bca3fa  ft/faq-page -> ft/faq-page
```

## Exercise 2

```bash
➜  bundle-1 git:(ft/faq-page) git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'
➜  bundle-1 git:(ft/home-page-redesign) git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
➜  bundle-1 git:(main) git commit -am 'add home page title'
[main 09b0f22] add home page title
 1 file changed, 1 insertion(+), 1 deletion(-)
➜  bundle-1 git:(main) git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 319 bytes | 159.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/jacob-js/thegym-git-exercise-bundle-1.git
   ebbcbb9..09b0f22  main -> main
➜  bundle-1 git:(main) git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'
➜  bundle-1 git:(ft/home-page-redesign) git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.
➜  bundle-1 git:(ft/home-page-redesign) git commit -am 'add home paragraph'
[ft/home-page-redesign b371843] add home paragraph
 1 file changed, 1 insertion(+)
➜  bundle-1 git:(ft/home-page-redesign) git push origin ft/home-page-redesign
Enumerating objects: 16, done.
Counting objects: 100% (16/16), done.
Delta compression using up to 4 threads
Compressing objects: 100% (14/14), done.
Writing objects: 100% (14/14), 1.50 KiB | 220.00 KiB/s, done.
Total 14 (delta 7), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (7/7), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/jacob-js/thegym-git-exercise-bundle-1/pull/new/ft/home-page-redesign
remote: 
To https://github.com/jacob-js/thegym-git-exercise-bundle-1.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
➜  bundle-1 git:(ft/home-page-redesign) 
```