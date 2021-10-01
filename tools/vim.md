# Vim

## Introduction

This tool really requires no introduciton. I started learning vi and vim (vImproved) when I started hacking in unix and linux. As it's a pretty ubiquitous text editor in those environments and insanely powerful, I've found that taking the effort to scale the steep learning curve is well worth the effort.

I'm constantly flabbergasted by how much powerful functionality has been packed into this editor and how relevant it still is today.

## Vim Commands

### View Registers

1. `:registers`

### Remove whitespace / left align

You can remove unwanted whitespace by using the following command:

`:%le`

### Write selected text out to a new file

1. Use visual mode to select text
2. Type `:` to go to ex mode
3. type `w <filename>` (include a full path if it needs to be written elsewhere than the current working directory)

### Macros

Macros are useful for recording a series of operations and then applying them repeatedly on new sections.

1. `q<letter to name macro>` to start recording operations to re-play 
1. `q` again to stop recording operations
1. `@<letter of named macro>` to 'playback' operations that were recorded
1. `<number>@<letter of named macro` to play the macro multiple times consecutively

### Terminal Commands

#### Shell commands

`CTRL+Z` will temporarily suspend vim and drop you onto the command line. Typing `fg` (for foreground) will bring you back into vim.

`r ! <terminal command>` will read the output of the terminal command into vim.

### Search commands

1. [How to search through a project folder recursively](https://stackoverflow.com/questions/7950558/how-can-i-search-a-word-in-whole-project-folder-recursively#7950649)

## Vim software/expansions

1. [The Ultimate Vim Configuration](https://github.com/amix/vimrc) - A collection of vimrc files and plugins that truly power-up your vim experience. Things like Pathogen (for installing vim packages), NERDTree (vim file explorer), Fugitive (Powerful Git integration), etc.
1. 

# Hacking Vim

## Vim as IDE

## commentary.vim plugin

This [plugin](https://github.com/tpope/vim-commentary) lets you comment code with motion commands.

- `gcc`: used to comment out a line. Takes a count
- `gc`: comment out target of motion, or selection in visual mode.
- `gcap`: as a specific example of the motion command above: comment out a paragraph

Finally, it is also possible to us it as part of a range `:7,17Commentary` or as part of a `:global` invocation like with `:g/TODO/Commentary`.


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

Add the following to your .vimrc:

`" functions for file extension '.pdf'.
function! NFH_pdf(f)
    execute '!open' a:f
    endfunction`


## NERDTree commands worth knowing

- To access the file management menu in NERDTree: type `m`. To create a new file type `a` and then type the filename. Append a `\` for a new directory.
- A simple `q` to close the NERDTree pane

## Miscellaneous Resources

