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
# To ssh://intranetserver:/home/git/bare_collab
#   1f8ec62..030bad7  master -> master

# 9463@R4402-1989014 MINGW64 ~/testgit/bare_collab (master)
# edit file on cygwin64 terminal
#  mycontent.txt
# Unchange first line from source = Not any more;) cygwin64terminal change
# Second line
# Third line
# Fourth line by cygwin64terminal
# 9463@R4402-1989014 ~/bare_collab
# $ git status
# On branch master
# Your branch is up to date with 'origin/master'.

# Changes not staged for commit:
#  (use "git add <file>..." to update what will be committed)
#  (use "git restore <file>..." to discard changes in working directory)
#        modified:   mycontent.txt
# $ git add .

# 9463@R4402-1989014 ~/bare_collab
#  $ git commit -m "cygwin64terminal change file"
# [master db9516e] cygwin64terminal change file
#  1 file changed, 2 insertions(+), 1 deletion(-)

# 9463@R4402-1989014 ~/bare_collab
# $ git log
# commit db9516ee0d0211b72515f04370021ef04da7a9fd (HEAD -> master)
# Author: puthaimuangway <thawinsak@192.168.246.45>
# Date:   Tue Jul 28 18:29:07 2020 +0700

#    cygwin64terminal change file

# commit 1f8ec62c5582a816dd0a0a7f9a42e9b64048e75a (origin/master, origin/HEAD)
# Author: thawinsak <thawinsak@git-cleint.itlab.com>
# Date:   Tue Jul 28 17:26:33 2020 +0700

#    Base commit from source

# 9463@R4402-1989014 ~/bare_collab
# $ git pull
# warning: Pulling without specifying how to reconcile divergent branches is
# discouraged. You can squelch this message by running one of the following
# commands sometime before your next pull:

#  git config pull.rebase false  # merge (the default strategy)
#  git config pull.rebase true   # rebase
#  git config pull.ff only       # fast-forward only

# You can replace "git config" with "git config --global" to set a default
# preference for all repositories. You can also pass --rebase, --no-rebase,
# or --ff-only on the command line to override the configured default per
#invocation.
# no changes added to commit (use "git add" and/or "git commit -a")
# remote: Counting objects: 3, done.
# remote: Compressing objects: 100% (2/2), done.
# remote: Total 3 (delta 0), reused 0 (delta 0)
# Unpacking objects: 100% (3/3), 306 bytes | 19.00 KiB/s, done.
# From ssh://intranetserver:/home/git/bare_collab
#   1f8ec62..030bad7  master     -> origin/master
# Auto-merging mycontent.txt
# CONFLICT (content): Merge conflict in mycontent.txt
# Automatic merge failed; fix conflicts and then commit the result.

# 9463@R4402-1989014 ~/bare_collab
# $ cat mycontent.txt
# <<<<<<< HEAD
# Unchange first line from source = Not any more;) cygwin64terminal change
# =======
# first line from source -- Changed by gitbash
# >>>>>>> 030bad7e84f7d7801a1eb68951e99fbac7992f4d
# Second line
# Third line
# Fourth line by cygwin64terminal
#$ git commit -m "Merge accept gitbash post"
#[master 3f60be2] Merge accept gitbash post

#9463@R4402-1989014 ~/bare_collab
#$ git log
#commit 3f60be2a4a0ba7af9f42b5195c3ebea5a6980a1b (HEAD -> master)
#Merge: db9516e 030bad7
#Author: puthaimuangway <thawinsak@192.168.246.45>
#Date:   Tue Jul 28 18:55:07 2020 +0700

#    Merge accept gitbash post

# commit db9516ee0d0211b72515f04370021ef04da7a9fd
# Author: puthaimuangway <thawinsak@192.168.246.45>
# Date:   Tue Jul 28 18:29:07 2020 +0700

#    cygwin64terminal change file

# commit 030bad7e84f7d7801a1eb68951e99fbac7992f4d (origin/master, origin/HEAD)
# Author: thawinsakclient <thawinsakk@pwa.co.th>
# Date:   Tue Jul 28 18:13:16 2020 +0700

#    gitbash first commit after changing the first lien

# commit 1f8ec62c5582a816dd0a0a7f9a42e9b64048e75a
# Author: thawinsak <thawinsak@git-cleint.itlab.com>
# Date:   Tue Jul 28 17:26:33 2020 +0700

#    Base commit from source

# 9463@R4402-1989014 ~/bare_collab
# git push
# git@192.168.246.45's password:
# Enumerating objects: 10, done.
# Counting objects: 100% (10/10), done.
# Delta compression using up to 4 threads
# Compressing objects: 100% (4/4), done.
# Writing objects: 100% (6/6), 704 bytes | 352.00 KiB/s, done.
# Total 6 (delta 0), reused 0 (delta 0), pack-reused 0
# To ssh://intranetserver:/home/git/bare_collab
#   030bad7..3f60be2  master -> master

# 9463@R4402-1989014 ~/bare_collab
# $ git log --graph
# *   commit 3f60be2a4a0ba7af9f42b5195c3ebea5a6980a1b (HEAD -> master, origin/master, origin/HEAD)
# |\  Merge: db9516e 030bad7
# | | Author: puthaimuangway <thawinsak@intranetserver>
# | | Date:   Tue Jul 28 18:55:07 2020 +0700
# | |
# | |     Merge accept gitbash post
# | |
# | * commit 030bad7e84f7d7801a1eb68951e99fbac7992f4d
# | | Author: thawinsakclient <thawinsakk@pwa.co.th>
# | | Date:   Tue Jul 28 18:13:16 2020 +0700
# | |
# | |     gitbash first commit after changing the first lien
# | |
# * | commit db9516ee0d0211b72515f04370021ef04da7a9fd
# |/  Author: puthaimuangway <thawinsak@intranetserver>
# |   Date:   Tue Jul 28 18:29:07 2020 +0700
# |
# |       cygwin64terminal change file
# |
# * commit 1f8ec62c5582a816dd0a0a7f9a42e9b64048e75a
#  Author: thawinsak <thawinsak@git-cleint.itlab.com>
# 9463@R4402-1989014 MINGW64 ~/testgit/bare_collab (master)
# $ git pull
# remote: Counting objects: 6, done.
# remote: Compressing objects: 100% (4/4), done.
# remote: Total 6 (delta 0), reused 0 (delta 0)
# Unpacking objects: 100% (6/6), 684 bytes | 2.00 KiB/s, done.
# From ssh://intranetserver:/home/git/bare_collab
#   030bad7..3f60be2  master     -> origin/master
# Updating 030bad7..3f60be2
# Fast-forward
#  mycontent.txt | 1 +
# 1 file changed, 1 insertion(+)

# 9463@R4402-1989014 MINGW64 ~/testgit/bare_collab (master)
# 9463@R4402-1989014 MINGW64 ~/testgit/bare_collab (master)
# $ git log
# commit 3f60be2a4a0ba7af9f42b5195c3ebea5a6980a1b (HEAD -> master, origin/master, origin/HEAD)
# Merge: db9516e 030bad7
# Author: puthaimuangway <thawinsak@intranetserver>
# Date:   Tue Jul 28 18:55:07 2020 +0700

#    Merge accept gitbash post

# commit db9516ee0d0211b72515f04370021ef04da7a9fd
# Author: puthaimuangway <thawinsak@192.168.246.45>
# Date:   Tue Jul 28 18:29:07 2020 +0700

#    cygwin64terminal change file

# commit 030bad7e84f7d7801a1eb68951e99fbac7992f4d
# Author: thawinsakclient <thawinsakk@pwa.co.th>
# Date:   Tue Jul 28 18:13:16 2020 +0700

#    gitbash first commit after changing the first lien

# commit 1f8ec62c5582a816dd0a0a7f9a42e9b64048e75a
# Author: thawinsak <thawinsak@git-cleint.itlab.com>
# ssh git@intranetserver
# [git@git-server ~]$
# home/git/collab_source
# [git@git-server collab_source]$
# [git@git-server collab_source]$ git remote add origin /home/git/bare_collab/
# [git@git-server collab_source]$ git pull  origin master
# From ../bare_collab
#  * branch            master     -> FETCH_HEAD
# * [new branch]      master     -> origin/master
# Updating 1f8ec62..3f60be2
# Fast-forward
# mycontent.txt | 3 ++-
# 1 file changed, 2 insertions(+), 1 deletion(-)
# [git@git-server collab_source]$















