## On servergit server intranet
##  mkdir collab_source
## cd collab_source/
## git init
## ls
## touch touch mycontent.txt
## add text to
## Unchange first line from source
## Second line
## Third line
## git clone --bare /home/git/collab_source/ /home/git/bare_collab
## cd bare_collab
## ls
## branches  config  description  HEAD  hooks  info  objects  packed-refs  refs
## on git bash client
## 9463@R4402-1989014 MINGW64 ~/testgit (master)
## $ git clone ssh://git@intranetserver:/home/git/bare_collab
## Cloning into 'bare_collab'...
## remote: Counting objects: 3, done.
## remote: Compressing objects: 100% (2/2), done.
## remote: Total 3 (delta 0), reused 0 (delta 0)
## Receiving objects: 100% (3/3), done.
## ls
## mycontent.txt


