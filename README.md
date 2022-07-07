## Create SSH

```
cd ~/.ssh
ssh-keygen -t ed25519
```

Then you'll see a prompt to name your ssh key. I'd suggest to use your account username + platform you're going to use it with. E.g. <developer.github>
```
Enter file in which to save the key (/home/user/.ssh/id_ed25519): <key name | e.g. johndoe.github>
```

Passphrase can be added at your convenience

```
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
```

When saved to the account you're now free to use this ssh key with all the available repositories.

## Clone Existing Repository
```
GIT_SSH_COMMAND="ssh -i ~/.ssh/johndoe.github" git clone git@github.com:username/repository.git
```

## Configure local repository to use specific ssh-key 
```
git config core.sshCommand "ssh -i ~/.ssh/johndoe.github"
