## Multiple accounts

1. Follow the above steps in [single account](single) and create two accounts: one & two

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

