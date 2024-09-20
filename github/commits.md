# Commits

*. Sometimes we need to revert file/directory to its previous commit
[how to revert a single file](https://dev.to/lofiandcode/git-and-github-how-to-revert-a-single-file-dha):

1. Make a copy to the file in case you change your mind.

2. Find the Commit ID (``git log``)

3. The command below will overwrite the current artifact (file or directory) state with the one from the [commit id]:

   ```shell
   git checkout [commit ID] -- path/to/artifact
   ```

*. Fast procedure how to examine commit and bring an artifact from it in the current branch:

1. Where are you:

   ```shell
   git branch -a
   * main
     ...
   ```

2. Find the Commit ID that you need to examine:

   ```shell
   git log
   ```

3. Create a new branch named <code>my_branch</code> for the commit:

   ```shell
   git checkout -b my_branch commit_id
   ```

4. After examination you found that you need to bring my_folder in to main branch:

   ```shell
   git checkout main
   git checkout [commit ID] -- my_folder
   ```

5. Do not forget to clean, i.e. remove my_branch:

   ```shell
   git branch -d my_branch
   ```

