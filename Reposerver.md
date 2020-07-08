# คู่มือ GIT
![](https://github.com/winkaew/githowto/blob/master/)
## การ Generate key ssh 
## อยู่ ที่ TERMINAL GIT BASH
## $ ssh-keygen
## $ ssh-copy-id  thawinsak@Servergit

## ขั้นตอนที่ 1 ติดตั้ง Gitbash
[การติดตั้ง gitbash](https://medium.com/touch-technologies/วิธีติดตั้ง-git-แบบง่ายๆ-ภายใน-3-นาที-3c8257127c40)
[คู่มือ GIT](https://git-scm.com/book/en/v2)

## $ git config --global --list
##  ฝั่ง SERVERGIT
## ssh thawinsak@servergit
## cd /home/git/gitpwa/gitpwadev
## mkdir testgit
## git init --bare
## ฝั่ง CLIENT  gitbash
## mkdir mygit
## cd mygit
## touch test.txt
## git add .
## git commit -m 'fist commit'
## git remote add origin ssh://thawinsak@servergit/home/git/pwagit/gitpwadev/testgit
## git push origin master
## ssh thawinsak@servergit 
## cd testgit
## git ls-tree --full-tree -r --name-only HEAD
## คู่มือ Version From Mastering git
## ssh git@servergit
## สร้าง ที่server mkdir /srv/git
## cd srv/git
##  git init --bare random.git
## client
## git clone ssh://git@servergit:/home/git/srv/git/random.git
## Cloning into random...
## Warning: You appear to have cloned an empty repository.
## create name program random.c
## git add random.c

## $ git status -s
## A  random.c
## ?? a.exe
## $ git commit -a -m "Initial  implementation"
## [master (root-commit) d38c870] Initial  implementation
## 1 file changed, 17 insertions(+)
##  create mode 100644 random.c
## -M พิมพ์ข้อความ -a หรือ -all ทั้งหมด 
## $ git push
## Enumerating objects: 3, done.
## Counting objects: 100% (3/3), done.
## Delta compression using up to 4 threads
## Compressing objects: 100% (2/2), done.
## Writing objects: 100% (3/3), 426 bytes | 142.00 KiB/s, done.
## Total 3 (delta 0), reused 0 (delta 0)
## To ssh://servergit:/home/git/srv/git/random.git
## * [new branch]      master -> master

## 9463@R4402-1989014 MINGW64 ~/mygitlocal/random (master)
## git log
## commit d38c87065429e8d09c052c49078bf334069f541d (HEAD -> master, origin/master)
## Author: thawinsakclient <thawinsakk@pwa.co.th>
##Date:   Wed Jul 8 11:48:37 2020 +0700

##    Initial  implementation

## 9463@R4402-1989014 MINGW64 ~/mygitlocal/random (master)
## $ git status -s
## ?? a.exe
##  แก้ไขไฟล์ เพิ่มเข้าไป #include <time.h>
## $ git status -s
##  M random.c
## ?? a.exe
## $ git diff
## warning: LF will be replaced by CRLF in random.c.
## The file will have its original line endings in your working directory
## diff --git a/random.c b/random.c
## index 8deb622..0fe2106 100644
## --- a/random.c
## +++ b/random.c
## @@ -1,5 +1,6 @@
##  #include <stdio.h>
##  #include <stdlib.h>
## +#include <time.h>  บรรทัดนี้เพิ่มเข้ามา จะมีเครื่องหมายบวก
## int random_int(int max)
## {
## return rand() % max;
## $ git commit -a -m "Initialize random number generator"
## warning: LF will be replaced by CRLF in random.c.
## The file will have its original line endings in your working directory
## [master 1f149de] Initialize random number generator
##  1 file changed, 1 insertion(+)
















