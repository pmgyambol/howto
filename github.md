## Single account
1. [Generate ssh key pairs for accounts](https://help.github.com/articles/generating-a-new-ssh-key/)

   ```shell
   ssh-keygen -t ed25519 -f ~/.ssh/[KEY_FILENAME] -C [USERNAME]
   ```

2. [Add them to GitHub accounts](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/).

   ```shell
   eval "$(ssh-agent -s)"
   ssh-add ~/.ssh/[KEY_FILENAME]
   more ~/.ssh/[KEY_FILENAME].pub
   ```
