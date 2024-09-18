# Pull options

Often we do not want directly to execute ''git pull''. Options:

1. [Examine the remote branch](https://stackoverflow.com/questions/3258243/check-if-pull-needed-in-git/3278427):

* Fastest and savetest:

```shell
git pull --dry-run
git status -uno
git show-branch *master
```

* [How to check for changes on remote (origin) Git repository](https://stackoverflow.com/questions/2514270/how-to-check-for-changes-on-remote-origin-git-repository)

* [How to "git pull" from master into the development branch](https://stackoverflow.com/questions/20101994/how-to-git-pull-from-master-into-the-development-branch)
