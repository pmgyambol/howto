## Single account

1. [Generate ssh key pairs for accounts](https://help.github.com/articles/generating-a-new-ssh-key/)

   ```shell
   ssh-keygen -t ed25519 -f ~/.ssh/[KEY_FILENAME] -C [USERNAME]
   ```

2. [Add the key to the GitHub account](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/).

   * Add the key locally to the ssh-agent

   ```shell
   eval "$(ssh-agent -s)"
   ssh-add ~/.ssh/[KEY_FILENAME]
   ```

   * [Add the key to the Github account](https://github.com/settings/keys): Icon > Dropdown menu > Settings > SSH and GPG keys + paste the content of:

   ```shell
   more ~/.ssh/[KEY_FILENAME].pub
   ```

3. Test / Troubleshoot

   ```shell
   ssh -T git@github.com
   more ~/.ssh/config
   git config -l
