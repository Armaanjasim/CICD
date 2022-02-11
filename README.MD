# CI/CD With Jenkins & Amazon Web Service

![Jenkins](Jenkins.PNG)

## Making A SSH Public Key
- Make sure you run gitbash as admin
- `cd ~/.ssh`
- `ssh-keygen -t rsa -b 4096 -C "armaanjasim@hotmail.co.uk"`
- After you press enter it will ask you "Enter file in which to save the key" and show you the file path of where it will save it by default if you do not change it. For the name I put `103a` and pressed enter
- It then ask "Enter passphrase (empty for no passphrase)" So you press enter twice and keep it empty
- This will then create two files in your .ssh folder `103a` and `103a.pub`
- After this you will want to `cat 103a.pub` and copy the information of this file exactly how it is.
- You will then take this copy over to github > `settings` >  `SSH and GPG keys` > `New SSH key` >  Enter a name of your choice `eng103a` > Paste the key of `103.pub`
- You can then create a new repository `CICD`
- Once you create a new repository follow the steps on github of setting it up using the `ssh` link and not the `https`.

### Blocker
- When setting up the repository I kept getting access denied. I thought it was to do with my ssh key being copied wrong onto github however the issue was to do with my gitbash terminal not identify my email. The way I fixed this was by using the command `ssh-add ~/.ssh/103a` and this added my email identity.


