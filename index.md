
# General
This repo to host the general notes and good to know facts.Mostly unordered in nature containing details related to projects which are work in progress.

QuickGuide
=======

  * [docker-gist](#docker-gist)
    * [golang-docker](#golang-docker)
  * [vim-cheat-sheet](#vim-cheat-sheet)
     * [vim-register-tips](#vim-register-tips)
  * [tmux-cheat-sheet](#tmux-cheat-sheet)
  * [ergodox-layout](#ergo-layout)
  * [misc](#misc)
  * [git-tips](#git-tips)
  * [coverage-buildstatus-report-tools](#coverage-buildstatus-report-tools)

# Docker-Gist
 
[Docker Skeleton-Gist][mygitgistdockerfile]

## Golang-Docker

[Golang-Dockernotes][golangdockernotes]

[Golang-official-Docker-img][golangofficialdockerimage]

# Vim-Cheat-Sheet
 
[vim cheat sheet][vimcheatsheet] 

## Vim-Register-tips

- Registers - They are used similar to clipboard instead of single version provided by system vim's memory buffer can be utilized as multiple clipboards.

- `:reg` command is used to display all the data held globally in all registers.
- `"<register name ex:a-z or 0-9>` command is used to display data held in provided register only.
- `"ay` command is used to copy the content yanked in to register a.
-  __NOTE:__ _use lower case register to replace contents already present in registers, upper case alphabets will append the data to registers_.

  further more details on default registers can be obtained via [vimregister][vimtipregister]

# Tmux-Cheat-Sheet

[tmux cheat sheet][tmuxcheatsheet]

# Ergo-Layout

[Ergolayout][ergodoxlayout]

[ErgolayoutUpd][ergodoxlayoutupd]


# misc

- In github markdown to add anchor to any heading use only lower case in the heading name (only in ToC section) and the link should be seperated using hypen.

# Coverage-Buildstatus-report-tools
[![Go Report Card](https://goreportcard.com/badge/github.com/etcd-io/etcd?style=flat-square)](https://goreportcard.com/report/github.com/etcd-io/etcd)
[![Coverage](https://codecov.io/gh/etcd-io/etcd/branch/master/graph/badge.svg)](https://codecov.io/gh/etcd-io/etcd)
[![Build Status Travis](https://img.shields.io/travis/etcd-io/etcdlabs.svg?style=flat-square&&branch=master)](https://travis-ci.com/etcd-io/etcd)
[![Build Status Semaphore](https://semaphoreci.com/api/v1/etcd-io/etcd/branches/master/shields_badge.svg)](https://semaphoreci.com/etcd-io/etcd)
[![Docs](https://img.shields.io/badge/docs-latest-green.svg)](https://etcd.io/docs)
[![Godoc](http://img.shields.io/badge/go-documentation-blue.svg?style=flat-square)](https://godoc.org/github.com/etcd-io/etcd)
[![Releases](https://img.shields.io/github/release/etcd-io/etcd/all.svg?style=flat-square)](https://github.com/etcd-io/etcd/releases)
[![LICENSE](https://img.shields.io/github/license/etcd-io/etcd.svg?style=flat-square)](https://github.com/etcd-io/etcd/blob/master/LICENSE)

# Git-tips
 - `git log` to display commit history for repo.
 - `git reset --hard <<commit hash or commit ref>>` to reverse the commits along with history and changes from stage.
 **NOTE:** Above command works only with unsynced/non pushed stage only changes.Any changes commited to remote(github) repo can not follow this approach.
 -  To preserve the changes in the current working folder even after reversing the commits follow below steps.
     - `git stash` - will capture the changes in cwd/pwd 
     - `git reset --hard <<commit hash or commit ref>>`- revert commit history along with changes in pwd.
     - `git stash pop` - re write the changes captured from step 1 to pwd.
     # Published commit reversal
       - `git revert <hash-or-ref>`- to revert published commits to remote repo.
     # Checkout previous commit
       - `git checkout <hash-or-ref>`- to checkout a published commit.
     
     
[mygitgistdockerfile]:https://gist.github.com/ehrktia/08527e17aff1d08df47fbb6305cba74a
[vimcheatsheet]:https://vim.rtorr.com
[tmuxcheatsheet]:https://tmuxcheatsheet.com
[ergodoxlayout]:https://configure.ergodox-ez.com/ergodox-ez/layouts/9DYOO/latest/2
[ergodoxlayoutupd]:https://configure.ergodox-ez.com/ergodox-ez/layouts/EewRQ/latest/2
[golangdockernotes]:https://blog.docker.com/2016/09/docker-golang/
[golangofficialdockerimage]:https://hub.docker.com/_/golang/
[vimtipregister]:https://www.brianstorti.com/vim-registers/
