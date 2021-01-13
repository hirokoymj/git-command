# Git command

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
