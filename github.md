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

3. Troubleshoot

   ```shell
   more ~/.ssh/config
   git config -l
   ```

## Multiple accounts

1. Follow the above steps and create two accounts: one & two

2. Create ~/.ssh/config:

   ```conf
   Host access-one
     Hostname github.com
     IdentityFile ~/.ssh/one

   Host access-two
     Hostname github.com
     IdentityFile ~/.ssh/two
   ```

3. Test

   ```shell
   ssh -T git@access-one
   ssh -T git@access-two

   git push git@access-one:one/<project>.git <branch>
   git push git@access-two:two/<project>.git <branch>

   git remote set-url origin git@access-one:one/<project>.git
   git remote set-url origin git@access-two:two/<project>.git
   ```

