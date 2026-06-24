### 1. Branching & The Golden Rule1
```bash
Initialized empty Git repository in C:/Users/Malaika/revisionforweb/.git/
PS C:\Users\Malaika\revisionforweb> git checkout -b feature/docs dev from it
PS C:\Users\Malaika\revisionforweb> git checkout -b feature/docs dev
PS C:\Users\Malaika\revisionforweb> git branch
Switched to a new branch 'feature/docs'
Switched to a new branch 'dev'
error: pathspec 'feature/docs' did not match any file(s) known to git
PS C:\Users\Malaika\revisionforweb> git checkout -b feature/docs
Switched to a new branch 'feature/docs'
PS C:\Users\Malaika\revisionforweb> git commit -m "GODisALL first commit start exercises"
[feature/docs (root-commit) f861302] GODisALL first commit start exercises 1 file changed, 15 insertions(+)
 create mode 100644 README.md
PS C:\Users\Malaika\revisionforweb> git remote add https://github.com/GODisALL-FriendOfJesus/revisionforweb.git
usage: git remote add [<options>] <name> <url>

    -f, --[no-]fetch      fetch the remote branches
    --[no-]tags           import all tags and associated objects when fetching
                          or do not fetch any tag at all (--no-tags)
    -t, --[no-]track <branch>
                          branch(es) to track
    --[no-]mirror[=(push|fetch)]
                          set up remote as a mirror to push to or fetch from

PS C:\Users\Malaika\revisionforweb> git remote add origin https://github.com/GODisALL-FriendOfJesus/revisionforweb.git
PS C:\Users\Malaika\revisionforweb> git push
fatal: The current branch feature/docs has no upstream branch.
    git push --set-upstream origin feature/docs

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\Malaika\revisionforweb> git push --set-upstream origin feature/docs
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 480 bytes | 80.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/GODisALL-FriendOfJesus/revisionforweb.git
 * [new branch]      feature/docs -> feature/docs
PS C:\Users\Malaika\revisionforweb> git push dev
fatal: Could not read from remote repository.
Please make sure you have the correct access rights
PS C:\Users\Malaika\revisionforweb> git push  origin --all
PS C:\Users\Malaika\revisionforweb> git branch -r
  origin/feature/docs
PS C:\Users\Malaika\revisionforweb> git branch
* feature/docs
error: pathspec 'dev' did not match any file(s) known to git
PS C:\Users\Malaika\revisionforweb> git checkout -b dev
PS C:\Users\Malaika\revisionforweb> git checkout feature/docs             
Switched to branch 'feature/docs'           
Your branch is up to date with 'origin/feature/docs'.
PS C:\Users\Malaika\revisionforweb> git branch
  dev
* feature/docs
PS C:\Users\Malaika\revisionforweb> git push origin --all
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/GODisALL-FriendOfJesus/revisionforweb/pull
To https://github.com/GODisALL-FriendOfJesus/revisionforweb.git
 * [new branch]      dev -> dev
PS C:\Users\Malaika\revisionforweb> git branch -r
  origin/feature/docs
PS C:\Users\Malaika\revisionforweb> git checkout feature/docs
M       README.md
Your branch is up to date with 'origin/feature/docs'.
PS C:\Users\Malaika\revisionforweb> git add .
PS C:\Users\Malaika\revisionforweb> git commit -m "GODisALL second changes are created"
[feature/docs 5c45d45] GODisALL second changes are created
 1 file changed, 56 insertions(+), 1 deletion(-)
PS C:\Users\Malaika\revisionforweb> git checkout dev
Switched to branch 'dev'
PS C:\Users\Malaika\revisionforweb>  


```
### 2. Decoding Merge Conflicts
```bash 

PS C:\Users\Malaika\revisionforweb> git add config.txtcise solving conflicts"
[dev 30b128f] GODisALL start of 2exercise solving conflicts
 create mode 100644 config.txt
PS C:\Users\Malaika\revisionforweb> git checkout -b feature/conflict
Switched to a new branch 'feature/conflict'
PS C:\Users\Malaika\revisionforweb> git add config.txt
PS C:\Users\Malaika\revisionforweb> git commit -m "GODisALL start of 2exer
[feature/conflict 1f68a5f] GODisALL start of 2exercise solving conflicts
 1 file changed, 1 insertion(+), 1 deletion(-)
M       README.md
Switched to branch 'dev'
Your branch is ahead of 'origin/dev' by 1 commit.
PS C:\Users\Malaika\revisionforweb> git add config.txtcise solving conflicts"
PS C:\Users\Malaika\revisionforweb> git merge feature/conflict
Auto-merging config.txt
Automatic merge failed; fix conflicts and then commit the result.
PS C:\Users\Malaika\revisionforweb> git add config.txt
PS C:\Users\Malaika\revisionforweb> git commit -m "GODisALL start of 2exercise well solved conflicts"
[dev 1c90335] GODisALL start of 2exercise well solved conflicts
PS C:\Users\Malaika\revisionforweb> git add README.md
PS C:\Users\Malaika\revisionforweb> git commit -m "GODisALL"
[dev b92c8c9] GODisALL
 1 file changed, 30 insertions(+), 1 deletion(-)
PS C:\Users\Malaika\revisionforweb> git push
Enumerating objects: 17, done.
Counting objects: 100% (17/17), done.
Delta compression using up to 4 threads
Compressing objects: 100% (11/11), done.
Writing objects: 100% (15/15), 1.82 KiB | 206.00 KiB/s, done.
Total 15 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
To https://github.com/GODisALL-FriendOfJesus/revisionforweb.git
   f5f91ad..b92c8c9  dev -> dev
PS C:\Users\Malaika\revisionforweb> 

```
### 3. Pull Requests & The Art of Review
```bash 
... subquestions were done in Website of git 


```
### 5 Hotfixes (Fires in Production)
```bash
PS C:\Users\Malaika\revisionforweb> git checkout main
PS C:\Users\Malaika\revisionforweb> git checkout -b mai
Switched to a new branch 'main'
PS C:\Users\Malaika\revisionforweb> git add app.js
PS C:\Users\Malaika\revisionforweb> git commit -m "GODisALL '(app.js file is created)'"
 1 file changed, 1 insertion(+)
PS C:\Users\Malaika\revisionforweb> git checkout -b hotfix/zero-fix main
Switched to a new branch 'hotfix/zero-fix'
Nothing specified, nothing added.addEmptyPathspec false"
PS C:\Users\Malaika\revisionforweb> git add app.js
PS C:\Users\Malaika\revisionforweb> git commit -m "GODisALL '(app.js file is created on hotfix)'"ated on hotfix)'
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\Malaika\revisionforweb> git checkout mainro-fix
Updating ba3c223..802596e
Fast-forward
 app.js | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\Malaika\revisionforweb> git checkout dev
Switched to branch 'dev'
Your branch is ahead of 'origin/dev' by 1 commit.
  (use "git push" to publish your local commits)
PS C:\Users\Malaika\revisionforweb> git merge hotfix/zero
merge: hotfix/zero - not something we can merge
PS C:\Users\Malaika\revisionforweb> 
```