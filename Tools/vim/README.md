set ts=3
set shiftwidth=3
set incsearch
set hlsearch
set cscopetag
set hlsearch
syntax on
set autoindent
set expandtab
set tags=/local/scratch/$USER/mtas_design//tags
set cursorline
set colorcolumn=110

set list
set listchars=tab:>-

highlight ColorColumn ctermbg=blue
highlight DiffAdd    cterm=bold ctermfg=10 ctermbg=17 gui=none guifg=bg guibg=Red
highlight DiffDelete cterm=bold ctermfg=10 ctermbg=17 gui=none guifg=bg guibg=Red
highlight DiffChange cterm=bold ctermfg=10 ctermbg=17 gui=none guifg=bg guibg=Red
highlight DiffText   cterm=bold ctermfg=10 ctermbg=88 gui=none guifg=bg guibg=Red

hi Search ctermbg=LightYellow
hi Search ctermfg=DarkRed