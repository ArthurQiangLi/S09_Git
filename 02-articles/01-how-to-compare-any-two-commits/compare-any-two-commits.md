
# Compare Any Two Commits with `git diff`

### 1. Compare Two Commits
```sh
git diff a1b2c3d 4e5f6g7 //this returns the difference in the cli windows, press 'q' to exit.
git diff a1b2c3d 4e5f6g7 //this returns a summary of X lines were added/removed in each file in the cli
```
This compares commit `a1b2c3d` with `4e5f6g7`.

### 2. Compare Two Commits focusing in a Specific File
This compares changes in `main.c` between the two commits.
```sh
git diff a1b2c3d 4e5f6g7 -- main.c
```

### 3. With Visual Tool
```sh
git difftool commit1 commit2
```
You need to config the difftool to Git before using it.
```sh
sudo apt install meld -y //install it for Linux.
git config --global diff.tool meld //set it as default git difftool
git config --global merge.tool meld //set it as default merge tool
git config --global difftool.prompt false //ensure Git does not prompt for confirmation every time
```

>[!note] for Windows, just run the installer and follow the setup instructions. From: 
https://meldmerge.org/ 

### 4. Generate a Patch File
This saves the differences as a patch file.
```sh
git diff commit1 commit2 > changes.patch
```

