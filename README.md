# How-to-change-message-and-author-of-old-commit-use-git-rebase
How to change message and author of old commit use git rebase


## STEP 1: Show log
```
git log
```


## STEP 2: Git rebase interactive
```
git rebase -i HEAD~N
```
or
```
git rebase -i --root
```

It will show a text editor like below:
```
pick 1223 ...
pick 1224 ...
```


## Step 3: Change pick -> edit of specific commit
If you want to amend commit 1234 -> Change editor like below
```
pick 1223 ...
edit 1224 ...
```

## Step 4a: If want to change message of choose commit
```
git commit --amend --m="New message" --no-edit
```
## Step 4b: If want to change author of choose commit
```
git commit --amend --author="Author Name <email@address.com>" --no-edit
```
## Step 5: Continue
```
git rebase --continue
```

## Step 6: Push force

```
git push -f
```