# Pull options

Often we do not want directly to execute ''git pull''. Options:

1. Examine:
   [check if pull is needed](https://stackoverflow.com/questions/3258243/check-if-pull-needed-in-git/3278427) and
   [check for changes](https://stackoverflow.com/questions/2514270/how-to-check-for-changes-on-remote-origin-git-repository)

   ```shell
   git pull --dry-run
   git status -uno
   git show-branch *main
   git remote show origin      # helps for throubleshoot too

   git diff  origin/main       # examine the diff
   git merge origin/main       # step by step accept every change 
   ```

1. [How to "git pull" from master into the development branch](https://stackoverflow.com/questions/20101994/how-to-git-pull-from-master-into-the-development-branch)
