##add usergit
su - git
$ ssh-keygen -t rsa
Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/9463/.ssh/id_rsa): thawinsak_id_rsa.pub
Enter passphrase (empty for no passphrase):
scp thawinsak_rsa.pub  root@IPxxxx:/home/git/thawinsak_rsa.pub
root@192.168.246.45's password:
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


