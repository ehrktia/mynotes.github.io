# Welcome to Ehrktia Notes

# General
This repo to host the general notes and good to know facts.Mostly unordered in nature containing details related to projects which are work in progress.

QuickGuide
=======

  * [docker-gist](#docker-gist)
    * [golang-docker](#golang-docker)
  * [golang-testing](#golang-testing)
  * [vim-cheat-sheet](#vim-cheat-sheet)
  * [tmux-cheat-sheet](#tmux-cheat-sheet)
  * [ergodox-layout](#ergo-layout)
  * [misc](#misc)

## Docker-Gist
 
[Docker Skeleton-Gist][mygitgistdockerfile]

## Golang-Docker

[Golang-Dockernotes][golangdockernotes]

[Golang-official-Docker-img][golangofficialdockerimage]

## Golang-Testing

[Advance-Golang-Testing][advancegolangtesting]

## Vim-Cheat-Sheet
 
[vim cheat sheet][vimcheatsheet]

[vim tricks 1][vimtricks1]

## Tmux-Cheat-Sheet

[tmux cheat sheet][tmuxcheatsheet]

## Ergo-Layout

[Ergolayout][ergodoxlayout]



### misc

- In github markdown to add anchor to any heading use only lower case in the heading name (only in ToC section) and the link should be seperated using hypen.

- Vimrc config obtained from https://github.com/joelhooks

```
"visual display of tabs and trailing space/characters
set listchars=nbsp:¬,tab:»·,trail:·
"savefile automatically
set autowrite
" For regular expressions turn magic on
set magic

" Show matching brackets when text indicator is over them
set showmatch
" Return to last edit position when opening files (You want this!)
autocmd BufReadPost *
     \ if line("'\"") > 0 && line("'\"") <= line("$") |
     \   exe "normal! g`\"" |
     \ endif
" Remember info about open buffers on close
set viminfo^=%

" Remap VIM 0 to first non-blank character
map 0 ^
" Breaking lines with \[enter] without having to go to insert mode (myself).
nmap <leader><cr> i<cr><Esc>
" Reload changes to .vimrc automatically
autocmd BufWritePost  ~/.vimrc source ~/.vimrc
" map ctrl p to open control p plugin
let g:ctrlp_map = '<c-p>'




```

[vimtricks1]:https://www.hillelwayne.com/post/intermediate-vim/?utm_source=hackernewsletter&utm_medium=email&utm_term=fav
[mygitgistdockerfile]:https://gist.github.com/ehrktia/08527e17aff1d08df47fbb6305cba74a
[vimcheatsheet]:https://vim.rtorr.com
[tmuxcheatsheet]:https://tmuxcheatsheet.com
[ergodoxlayout]:https://configure.ergodox-ez.com/ergodox-ez/layouts/B4ZZd/latest/1

[golangdockernotes]:https://blog.docker.com/2016/09/docker-golang/
[golangofficialdockerimage]:https://hub.docker.com/_/golang/
[advancegolangtesting]:https://medium.com/@povilasve/go-advanced-tips-tricks-a872503ac859
