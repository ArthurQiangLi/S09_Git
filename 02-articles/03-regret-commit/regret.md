# Undo last commit when regret


## 1. KEEP THE CODE CHANGES STAGED
```sh
git reset --soft HEAD~1

git commit -m 'commit again'

```


This below will delete the last commit, no changes staged
```sh
git reset --hard HEAD~1
```


This below Just modifies the last commit message

```sh
git commit --amend -m "new message for last commit"

```


## 2. You pushed last commit to Github and regret?


You can modify it and do another commit (this doesn't rewrite history). Or you can rewrite history by:

```sh
#Undo last commit and get the changes staged locally
git reset --soft HEAD~1 # --hard will discard the changes.
git push --force


# Change last commit message only
git commit --amend -m "New message"
git push --force


```

> `--force` rewrites history on GitHub. Anyone else who pulled will need to fix their local branch manually.

# END