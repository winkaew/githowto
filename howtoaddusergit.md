##คู่มือการใช้งาน GIT

1. คำสั่งในการสร้าง Key RSA สำหรับ git
su - git
$ ssh-keygen -t rsa
Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/9463/.ssh/id_rsa): thawinsak_id_rsa.pub (กรอกเป็นชื่อไฟล์)
Enter passphrase (empty for no passphrase): ใส่คำสำคัญที่เราต้องการ 2 ครั้ง

2. ขั้นตอนการดำเนินการเปิดใช้งาน Key ที่สร้างในระบบ
scp thawinsak_rsa.pub  root@IPxxxx:/home/git/thawinsak_rsa.pub
root@IPserver's password:
thawinsak_rsa.pub                             100%  572    10.6KB/s   00:00
[git@git-server ~]$ cat ~/thawinsak_rsa.pub  >>~/.ssh/authorized_keys
[git@git-server ~]$ sudo groupadd gituser

3. ขั้นตอนการสร้าง folder git

3.1 การล็อกอิน และการกำหนด User git 
[sudo] password for git:
[git@git-server ~]$
sudo usermod -a -G gituser git
[git@git-server ~]$ cd ~git
[git@git-server ~]$ pwd
/home/git

3.2 การสร้าง Folder สำหรับเก็บ code ใน git 
[git@git-server gitpwa]$ mkdir gitpwadev
[git@git-server gitpwa]$ mkdir gitpwamobile
[git@git-server gitpwa]$ mkdir gitpwaweb
[git@git-server gitpwa]$ ls
gitpwadev  gitpwamobile  gitpwaweb
[git@git-server gitpwa]$ pwd
/home/git/gitpwa

3.3 การกำหนด Sharing Directory ของ git 
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

3.4 การ clone และการ push code เข้าไปใน git
9463@R4402-1989014 MINGW64 ~/mygit/callcenter
$ git clone ssh://root@Ipserver:/home/git/gitpwa/gitpwadev/.
Cloning into '.'...
root@192.168.246.45's password:
warning: You appear to have cloned an empty repository.

9463@R4402-1989014 MINGW64 ~/mygit/callcenter (master)
$ ls

9463@R4402-1989014 MINGW64 ~/mygit/callcenter (master)
$ pwd
/c/Users/9463/mygit/callcenter

9463@R4402-1989014 MINGW64 ~/mygit/callcenter (master)
$git remote rm 
9463@R4402-1989014 MINGW64 ~/mygit/callcenter/PWAWebUser (master)
$ git commit -m "test commit"
On branch master
nothing to commit, working tree clean

9463@R4402-1989014 MINGW64 ~/mygit/callcenter/PWAWebUser (master)
$ git status
On branch master
nothing to commit, working tree clean

9463@R4402-1989014 MINGW64 ~/mygit/callcenter/PWAWebUser (master)
$ git push
fatal: The current branch master has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin master


9463@R4402-1989014 MINGW64 ~/mygit/callcenter/PWAWebUser (master)
$ git push origin master
Enumerating objects: 299, done.
Counting objects: 100% (299/299), done.
Delta compression using up to 4 threads
Compressing objects: 100% (285/285), done.
Writing objects: 100% (299/299), 2.41 MiB | 2.19 MiB/s, done.
Total 299 (delta 23), reused 0 (delta 0)
remote: Resolving deltas: 100% (23/23), done.
To 192.168.246.45:/home/git/gitpwa/gitpwadev/callcenter/pwawebuser
 * [new branch]      master -> master

9463@R4402-1989014 MINGW64 ~/mygit/callcenter/PWAWebUser (master)
$






