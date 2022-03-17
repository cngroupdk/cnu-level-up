# Feature branch workflow

## 1. Start from master branch with latest changes

```
git checkout master
git pull
```

## 2. Create a feature branch for your work

- naming your branches - use prefix `feature`, `fix`, `dev`

```
git checkout -b feature/new-feature
```

## 3. Commit your work

- try not to do everything in one commit, but make commit after every finished increment of your work

```
git status
git add .
git commit //for every commit add meaningful message (ex. “Modified getAllBlogs endpoint”)
```

## 4. After you’re done, push your changes to remote

```
git push -u origin feature/new-feature
```

## 5. Create pull request

- now your work will be reviewed by your teammates
- locally resolved their remarks and push the changes

## 6. Merge pull request back to the master branch

- merge vs. rebase
- your should rebase and squash your feature branch

```
git checkout master
git pull
git checkout feature/new-feature
git merge master // now you merged the latest changes from master to your branch
```

- resolved any conflicts

```
git push // now your feature branch is ready to be rebased to master
```

- you can rebase and squash it via Github UI and close the pull request

Read more at [Atlassian Git Tutorials](https://www.atlassian.com/git/tutorials/comparing-workflows)
