# Vim notes and cheatsheet


## Surround plugin
* `S` - in Visual mode, will insert surrounding tags outside selection

## Tabs
* `vim -p somefile.js somefile.html` - opens files in tabs
* `:tabe someOtherFile.js - opens file` in a new tab while in Vim
* `gt` - moves one tab forward
* `gT` - moves one tab backward
* `2gt` - moves you to the second tab
* `3gt` - moves you to the third tab

## Indenting
* `==` - indents code properly
* `5==` - indents 5 lines of code properly

## Misc Commands
* `+` and `-` take you up and down, but start you at the first whitespace character
* `C` - clears everything to the right of the cursor
* `:vsp` - vertical split

## Marks
* `ma` - creates a mark called "a"
* to go there, hit: `\`a`
* `\`.` will take you to the last place you were

## Page Navigation
* `ctrl-f` - forward a whole page
* `ctrl-b` - back a whole page
* `ctrl-d` - down 1/2 a page
* `ctrl-u` - up 1/2 a page

* `50G` - takes you to line #50

##`Search
* `\*'` - searches on the word that you're in
* `Shift-I` - starts insert mode at the beginning of the line you're on
* `Shift-A` - starts insert mode at the end of the line

## Basic Commands
* `o` - inserts a line below and changes mode to insert
* `shift-o` - inserts a line above and changes mode to insert

## Deleting
* `x` - deletes whatever is under the cursor
* `X` - deletes whatever is before the cursor
* `dd` - deletes current line
* `dw` - deletes word
* `de` - deletes to end of word without deleting the space
* `dap` = delete around paragraph

* `r` - replace one character
* `R` - changes to replace mode
* `shift-Y` - yanks a whole line
* `p` - puts after the cursor
* `shift-p` - puts before the cursor
* `J` - join lines
* `gJ` - join lines without space between

## Selection
* `V` - makes selections by line
* `ctrl-v` - selects fist column in visual block mode
* `ctrl-v` then r - replaces all of the selection with characters
* `ctrl-v` then I then spaces then escape - inserts spaces in front of everything
* `ctrl-v` - puts you in visual block mode, I then enter spaces etc.
* `:noh` - clears search highlighting

## Buffers
* `:ls` - lists buffers
* `:ls` - lists hidden buffers too
* `:help` - brings up help documentation
* `:b#` - takes you to the last used buffer
* `:b 4` - takes you to the buffer that begins with the number 4
* `:b index.html` - fills the buffer with that filename
* `:bd` - deletes the current buffer
* `:22,24bd` - deletes the range of buffers between 22 and 24
* `:$bd` - deletes all buffers

## Buffer window management
* `ctrl-w-o` - makes this the only window
* `ctrl-w-j` - moves to the bottom window
* `ctrl-w-k` - moves to the top window etc.
* `ctrl-w-v` - makes a vertical split
* `ctrl-w,shift-h` - moves the current buffer to the left
* `ctrl-w, shift-j` - moves the current buffer to the bottom etc.
* `ctrl-w,p` - moves between the last window used
* `ctrl-w` - will cycle through windows

## My Leader Commands
* my leader key is now set to `,`
* `<leader>-c` = toggle comments on currently selected line or visual selection
* `<leader>-nt` = toggles showing NerdTree

## Pasting
* `F2` - toggle indentation to make pasting work normally

## Recording
* `q` `letter` - begin recording
* `q` - end recording
