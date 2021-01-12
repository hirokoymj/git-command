# Git command

## Daily development Git command
1. Check your current branch.
	```js
	git branch
	``` 

2. Create your branch. A new created branch is the copy of your current branch.
	```
	git branch my-test-branch
	```

3. Switch new branch.
   
   ```js
	 git checkout my-test-branch
	 ```

3. Change code.
4. Commit your changes. Your changes are saved in `Staging Area`

```js
git status
git add .
git commit -m "added new function"
```

5. Push your change to remote repository

```js
git push origin [your branch name0]
```

6. Login GitHub and check to see if your branch exists. 