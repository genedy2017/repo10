# Developer wants to work on new feature  (f202)

1. `git pull`
2. `git checkout -b f202`
3. `git commit -a -m "Working on feature 202"`
4. `git commit -a -m "Finished feature 202"`
5. `git push origin f202`
6. Make a pull request
7. Project manager asks for a modification
8. `git commit -a -m "Pull request updated"`
9. Project manager accepts pull request (f202 branch merged to master branch on origin)
10. `git checkout master`
11. `git pull`

# Resolving conflicts
On _f116_ branch, developer got notification of update on remote _master_:

```
git checkout master
git pull
git checkout f116
git merge master
```

* If conflict is reported, fix it and then:

```
git add *
git merge --continue
```

Or alternatively:

```
git commit -a -m "Fixing conflict"
```

# Deleting a remote branch

```
git push origin --delete f112
```


