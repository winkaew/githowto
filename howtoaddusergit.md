##add usergit
su - git
$ ssh-keygen -t rsa
Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/9463/.ssh/id_rsa): thawinsak_id_rsa.pub
Enter passphrase (empty for no passphrase):
scp thawinsak_rsa.pub  root@IPxxxx:/home/git/thawinsak_rsa.pub
root@IPserver's password:
thawinsak_rsa.pub                             100%  572    10.6KB/s   00:00
[git@git-server ~]$ cat ~/thawinsak_rsa.pub  >>~/.ssh/authorized_keys
[git@git-server ~]$ sudo groupadd gituser

We trust you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

    #1) Respect the privacy of others.
    #2) Think before you type.
    #3) With great power comes great responsibility.

[sudo] password for git:
[git@git-server ~]$
sudo usermod -a -G gituser git
[git@git-server ~]$ cd ~git
[git@git-server ~]$ pwd
/home/git
[git@git-server gitpwa]$ mkdir gitpwadev
[git@git-server gitpwa]$ mkidr gitpwamobile
-bash: mkidr: command not found
[git@git-server gitpwa]$ mkidir gitpwamobile
-bash: mkidir: command not found
[git@git-server gitpwa]$ mkdir gitpwamobile
[git@git-server gitpwa]$ mkdir gitpwaweb
[git@git-server gitpwa]$ ls
gitpwadev  gitpwamobile  gitpwaweb
[git@git-server gitpwa]$ pwd
/home/git/gitpwa
[git@git-server gitpwa]$
[git@git-server gitpwadev]$ git init --bare --shared=group
Initialized empty shared Git repository in /home/git/gitpwa/gitpwadev/
[git@git-server gitpwadev]$ ls
branches  config  description  HEAD  hooks  info  objects  refs
[git@git-server gitpwadev]$ ls
branches  config  description  HEAD  hooks  info  objects  refs
[git@git-server gitpwadev]$ rm -rf *
[git@git-server gitpwadev]$ ls
[git@git-server gitpwadev]$ ls
[git@git-server gitpwadev]$ ls
[git@git-server gitpwadev]$ mkdir callcenter
[git@git-server gitpwadev]$ ls
callcenter
[git@git-server gitpwadev]$ cd callcenter
[git@git-server callcenter]$ git init --bare --shared=group
Initialized empty shared Git repository in /home/git/gitpwa/gitpwadev/callcenter/
[git@git-server callcenter]$
/home/git/gitpwa/gitpwadev/callcenter
[root@git-server callcenter]# chgrp -R gituser /home/git/gitpwa/gitpwadev/callcenter/
[root@git-server callcenter]# chmod -R g+rw /home/git/gitpwa/gitpwadev/callcenter/
[root@git-server callcenter]# chmod g+s `find /home/git/gitpwa/gitpwadev/callcenter/ -type d `
[root@git-server callcenter]#
 chmod g+s /home/git/gitpwa/gitpwadev/
 [git@git-server gitpwadev]$ git init --bare --shared=group
Initialized empty shared Git repository in /home/git/gitpwa/gitpwadev/
[git@git-server gitpwadev]$
 git close ssh://192.168.246.45:/home/git/gitpwa/gitpwadev/.
git: 'close' is not a git command. See 'git --help'.

The most similar command is
        clone






