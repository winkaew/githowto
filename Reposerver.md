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







