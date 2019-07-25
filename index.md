
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

  further more details on default registers can be obtained via [vimregister][vimtipregister]<br>
   **More Tips**
   
   Hit Ctrl-R then `".` If you have literal control characters in what you have yanked, use Ctrl-R, Ctrl-O `".`<br>
	•  0 (yank register: when you use y in normal mode, without specifying a register, yanked text goes there and also to the default register)<br>
	•  1 to 9 (shifting delete registers, when you use commands such as c or d, what has been deleted goes to register 1, what was in register 1 goes    register 2, etc.)<br>
	•    `"` (default register, also known as unnamed register. This is where the `"` comes in Ctrl-R, `"`)<br>
	•    a to z for your own use (capitalized A to Z are for appending to corresponding registers).<br>
	•    `_` (acts like /dev/null (Unix) or NUL (Windows), you can write to it but it's discarded and when you read from it, it is always empty)<br>
	•    `-` (small delete register)<br>
	•    `/` (search pattern register, updated when you look for text with `/, ?, * or #` for instance; you can also write to it to dynamically change the search pattern)<br>
	•   `:` (stores last VimL typed command via Q or `:,` readonly)<br>
	•   `+ and *` (system clipboard registers you can write to them to set the clipboard and read the clipboard contents from them)<br>
	•  In normal mode, hit `":p`. The last command you used in vim is pasted into your buffer.<br>
 
 Let's decompose: `"` is a Normal mode command that lets you select what register is to be used during the next yank, delete or paste operation. So `":` selects the colon register (storing last command). Then p is a command you already know, it pastes the contents of the register.<br>
 command - `yj:@"Enter`<br>
*  `:@` Ex command plays Ex commands stored in the register given as argument, and `"` is how you refer to the unnamed register. <br>
•  If you have recorded a macro with `qa...q` then `:echo @a` will tell you what you have typed, and `@a` will replay the macro (probably you knew that one, very useful in order to avoid repetitive tasks)<br>


Further reading on same from Stack overflow is on -[vim_reg_moretips][vim_reg_moretips]

   
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
[vim_reg_moretips]:https://stackoverflow.com/questions/3997078/how-to-paste-yanked-text-into-vim-command-line/3997110#3997110
