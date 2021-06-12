# Vim

## Introduction

This tool really requires no introduciton. I started learning vi and vim (vImproved) when I started hacking in unix and linux. As it's a pretty ubiquitous text editor in those environments and insanely powerful, I've found that taking the effort to scale the steep learning curve is well worth the effort.

I'm constantly flabbergasted by how much powerful functionality has been packed into this editor and how relevant it still is today.

## Vim Commands

### Search commands

1. [How to search through a project folder recursively](https://stackoverflow.com/questions/7950558/how-can-i-search-a-word-in-whole-project-folder-recursively#7950649)

## Vim software/expansions

1. [The Ultimate Vim Configuration](https://github.com/amix/vimrc) - A collection of vimrc files and plugins that truly power-up your vim experience. Things like Pathogen (for installing vim packages), NERDTree (vim file explorer), Fugitive (Powerful Git integration), etc.
1. 

# Hacking Vim

## Vim as IDE

## Markdown

To configure using OSX's Marked 2 as the standard for opening a PDF file from Vim, at the following command to your .vimrc:

`:nnoremap <leader>m :silent !open -a Marked\ 2.app '%:p'<cr>`

This will ensure the `<leader>m` will open the current markdown file in Marked 2.

In case this messes with the rendering of the file and the command for a reload is the `:edit` override: `:e!`

## Navigating Links

- `gx`: Open a link
- `gf`: goto file
- `Ctrl+6`: return to previous file

## Opening a PDF

Add the followin to your .vimrc:

`" functions for file extension '.pdf'.
function! NFH_pdf(f)
    execute '!open' a:f
    endfunction`


## NERDTree commands worth knowing

- To access the file management menu in NERDTree: type `m`. To create a new file type `a` and then type the filename. Append a `\` for a new directory.
- A simple `q` to close the NERDTree pane

## Miscellaneous Resources




