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
## on Cygwin64 Terminal 
## git clone ssh://git@intranetserver:/home/git/bare_collab
## ls
## $ ls
## mycontent.txt
## edit mycontent.txt
## first line from source -- Changed by gitbash
## Second line
## Third line
## $ git status
## On branch master
## Your branch is up to date with 'origin/master'.

## Changes not staged for commit:
##  (use "git add <file>..." to update what will be committed)
##  (use "git restore <file>..." to discard changes in working directory)
##        modified:   mycontent.txt

## no changes added to commit (use "git add" and/or "git commit -a")
9463@R4402-1989014 MINGW64 ~/testgit/bare_collab (master)
$ git add .

9463@R4402-1989014 MINGW64 ~/testgit/bare_collab (master)
$ git commit -m "gitbash first commit after changing the first lien "
[master 030bad7] gitbash first commit after changing the first lien
 1 file changed, 1 insertion(+), 1 deletion(-)

## 9463@R4402-1989014 MINGW64 ~/testgit/bare_collab (master)
## $ git log
## commit 030bad7e84f7d7801a1eb68951e99fbac7992f4d (HEAD -> master)
## Author: thawinsakclient <thawinsakk@pwa.co.th>
## Date:   Tue Jul 28 18:13:16 2020 +0700

##    gitbash first commit after changing the first lien

## commit 1f8ec62c5582a816dd0a0a7f9a42e9b64048e75a (origin/master, origin/HEAD)
## Author: thawinsak <thawinsak@git-cleint.itlab.com>
## Date:   Tue Jul 28 17:26:33 2020 +0700

##    Base commit from source

## 9463@R4402-1989014 MINGW64 ~/testgit/bare_collab (master)
# $
# 9463@R4402-1989014 MINGW64 ~/testgit/bare_collab (master)
# $ git pull
# Already up to date.
# $ git push
# Enumerating objects: 5, done.
# Counting objects: 100% (5/5), done.
# Delta compression using up to 4 threads
# Compressing objects: 100% (2/2), done.
# Writing objects: 100% (3/3), 326 bytes | 163.00 KiB/s, done.
# Total 3 (delta 0), reused 0 (delta 0)
# To ssh://serverintranet:/home/git/bare_collab
#   1f8ec62..030bad7  master -> master

# 9463@R4402-1989014 MINGW64 ~/testgit/bare_collab (master)
# $






