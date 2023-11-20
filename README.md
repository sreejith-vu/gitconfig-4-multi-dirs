# gitconfig-4-multi-dirs
## Isolate Work and Personal Spaces using GITCONFIG

### Create .gitconfig with below contents at root/home directory
```
[includeIf "gitdir:~/PERSONAL/"]
path = ~/PERSONAL/.gitconfig
 
[includeIf "gitdir:~/WORK/"]
path = ~/WORK/.gitconfig
 
[core]
excludesfile = ~/.gitignore  
```

### mkdir ~/PERSONAL and add .gitconfig with below content inside 
```
[user]
email = xx@xx.com
name  = xx
 
[core]
sshCommand = "ssh -i ~/.ssh/id_ed25519_personal"
```
### mkdir ~/WORK and add .gitconfig with below content inside 

```
[user]
email = xx@xx.com
name  = xx

[core]
sshCommand = "ssh -i ~/.ssh/id_ed25519_work"
```
### Now create SSH keys with respective names and update those in GIT UI and try git clone
