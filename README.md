# Git command

## git pull --rebase



https://stackoverflow.com/questions/2472254/when-should-i-use-git-pull-rebase

>sometimes--by whatever reason--you think that it would actually be better if these two--remote and local--were one branch. Like in SVN. It is here where git pull --rebase comes into play. You no longer merge--you actually commit on top of the remote branch. That's what it actually is about.

1. (develop) git pull                     // Gets the latest develop
2. (my-branch) git checkout my-branch     // Switch a branch
3. (my-branch) git pull origin develop  // REBASE BETWEEN develop and my-branch.
4. (my-branch) ==== When conflicts happens, fix them manually. 
6. (my-branch) git add .
5. (my-branch) git rebase --continue
7. (my-branch) git reset origin/develop // SQUASH MULTIPLE COMMITS HERE!!! 
8. (my-branch) git add .
9. (my-branch) git commit -m 'some commit message'
10. (my-branch) git push my-branch --no-verify --force


## Daily development flow

1. Check your current branch.

   ```js
   git branch
   ```

2. Create your branch. A new branch is the copy of your current branch.

   ```
   git branch my-test-branch
   ```

3. Switch the branch that you created.

   ```js
    git checkout my-test-branch
   ```

4. Change code.

5. Commit your changes. Your changes are saved in `Staging Area`

   ```js
   git status
   git add .
   git commit -m "added new function"
   ```

6. Push your change to remote repository

   ```js
   git push origin [your branch name]
   ```

7. Login GitHub and check to see if your branch exists.

## Merge

Trying to merge `test-branch` to `master` branch.

1. Check if you are currently master branch.
   ```js
   git branch
   ```
2. Merge `test-branch` to `master`
   ```js
   git merge test-branch
   ```
3. Push the upated master branch to remote repository
   ```js
   git push origin master
   ```

## Pull

Get the latest code from remote repository so your local repository could be updated. When your co-workers update a master branch, you should get the latest one!

```js
git pull master
```

## Stash

Using `stash` command, you can hold your all changes temporary and makes clean working directory. So you can merege the latest master into your own branch.

```js
git stash //-----> Hold all your changes and your branch becomes clean.
git merge master //---> you can merge the latest master here!
git stash apply	// ---> Changed back to your changes.
```

## Log

Trying to see the git log.

```js
git log ---graph --oneline
```

## Remove remote repository

```js
git remote origin [remote-repo-name]
```

## Show remote repository in your local

```js
git remote show origin
```
 


## git reset HEAD^

https://dzone.com/articles/git-reset-head



## git cherry-pick <commit-hash>
   


