# Check a Repo Size (Locally)


The command to check github remote size is very complicated, and not handy. Thus, we  don't talk about it in this article.

## Use `du` cmd to see folder sizer

```sh

du -sh .  //see all size 
31M     .
du -sh .git 
13M     .git
```

In on Windows, you need to use `Bash` terminal to use this `du` command. 


## Use git cmd to see a breakdown

```sh
git count-objects -vH
count: 0
size: 0 bytes //loose objects
in-pack: 51
packs: 1
size-pack: 12.33 MiB //compressed size of objects
prune-packable: 0
garbage: 0
size-garbage: 0 bytes

```



# END