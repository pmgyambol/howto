# Commits

Sometimes we need to revert file/directory to its previous commit
[how to revert a single file](https://dev.to/lofiandcode/git-and-github-how-to-revert-a-single-file-dha):

1. Make a copy to the file in case you change your mind.

2. Find the Commit ID (``git log``)

3. The command below will overwrite the current file state with the one from the [commit id]:

   ```shell
   git checkout [commit ID] -- path/to/file
   ```
