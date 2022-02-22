# VIM notes

Following document illustrates my most used vim commands.

## Vim / Neovim basic commands

### Modes

| Command    | Function                                      |
| ---------- | --------------------------------------------- |
| Esc        | Normal mode                                   |
| Esc-i      | Insert mode                                   |
| Esc-v      | Visual mode                                   |
| Esc-V      | Visual row mode                               |
| Esc-CTRL-v | Visual block mode                             |
| Esc-R      | Enters replace mode (Overwrites under cursor) |

### Cursor movements

| Command | Function                                         |
| ------- | ------------------------------------------------ |
| hjkl    | Move cursor left, down, up, right                |
| w       | Move forward to the beginning of a word          |
| e       | Move to the end of a word                        |
| b       | Move backward to the beginning of a word         |
| 3w      | Move forwards three words (beginning of a word)  |
| 3e      | Move forwards three workds (end of a word)       |
| 3b      | Move backwards three words                       |
| 0       | Cursor to the beginning of line                  |
| $       | Move to end end of the line                      |
| )       | Jump forward one sentence                        |
| (       | Jump backward one sentence                       |
| }       | Jump forward one paragraph                       |
| {       | Jump backward a paragraph                        |
| j       | Jump forward one line                            |
| 10j     | Jump forward 10 lines                            |
| k       | Jump backward one line                           |
| 10k     | Jump backward 10 lines                           |
| H       | Jump to the top of the screen                    |
| M       | Jump to the middle of the screen                 |
| L       | Jump to bottom of screen                         |
| CTRL-f  | Scroll forward one screen                        |
| CTRL-b  | Scroll backward one screen                       |
| CTRL-d  | Scroll forward half screen                       |
| CTRL-u  | Scroll backward half screen                      |
| G (n)   | Move cursor to EOF                               |
| gg (n)  | Move cursor to top of file                       |
| nG      | Go to given line n                               |
| z ENTER | Move current line to top of screen and scroll    |
| z.      | Move current line t center of screen and scroll  |
| z-      | Move current line to bottom of screen and scroll |
| Enter   | Move to first character of next line             |
| j$      | Put the cursor at the end of next line           |

### Edit

| Command        | Function                                             |
| -------------- | ---------------------------------------------------- |
| i              | Inserts text at the left to cursor                   |
| a              | Inserts text at the right to cursor                  |
| I              | Insert at the start of the current line              |
| A              | Insert at the end of the current line                |
| o              | Insert a line below current line                     |
| O              | Insert a line above the current line                 |
| s (cl)         | Delete character under cursor and start insert       |
| S (cc)         | Delete all text line and start insert at beg of line |
| C (c$)         | Delete everything right to the cursor and insert     |
| cw             | Delete to the end of word and start inserting        |
| ce             | Delete rest of the word under and right to cursor    |
| ciw            | Delete a word and insert                             |
| rx             | Replace the character under the cursor with 'x'      |
| u              | Undo                                                 |
| U              | Undo all edits on a row                              |
| CTRL-r         | Redo                                                 |
| J              | Joins the current line with the line below           |
| CTRL-v shift I | Enter text in block mode                             |
| ea             | Move cursor to end of word and edit                  |
| `z=`           | Spell suggestions (in markdown)                      |
| `<C-V><C-I>`   | Select block and insert into block                   |
| `gq`           | Select with `<Shift-v>` and gq will wrap line        |
| `viw`          | Select word under cursor                             |

### Cut, copy and paste

| Command | Function                               |
| ------- | -------------------------------------- |
| y       | Yank character                         |
| yaw     | Yank a word                            |
| yw      | Yank word                              |
| y3w     | Yank three words                       |
| yy      | Yanks whole line                       |
| 1,10y   | Yanks row 1 - 10                       |
| d       | Cut text                               |
| dd      | Cut whole line                         |
| P       | Put before cursor                      |
| p       | Put after cursor                       |
| jk (v)  | Select lines up or down in visual mode |
| CTRL-V  | Paste from clipboard                   |
| `"*y`   | Copy to clipboard                      |

### Deletion

| Command   | Function                                           |
| --------- | -------------------------------------------------- |
| d         | Delete operator                                    |
| dw        | Delete a word (cursor needs to be at beg of word)  |
| de        | Delete a word                                      |
| daw       | Delete a word (irrespective where cursor is)       |
| d2w       | Delete 2 words                                     |
| d4w (n)   | Deletes 4 words                                    |
| d4e (n)   | Deletes 4 words                                    |
| dd (n)    | Delete whole line                                  |
| 2dd (n)   | Delete two lines                                   |
| d$        | Delete the rest of the line - right of the cursor  |
| c$        | Delete the rest of the line right from cursor      |
| D (d$)    | Delete to end of the line                          |
| x (dl)    | Delete character under the cursor                  |
| 4x        | Deletes 4 characters                               |
| X (dh)    | Delete character left of the cursor                |
| dG        | Delete until the end of line                       |
| dgg       | Delete until the start of line                     |
| dw then p | When you delete, text is saved. Use p for put back |

### Working with files

| Command         | Function                                            |
| --------------- | --------------------------------------------------- |
| :w FILENAME     | Writes the currrent vim file to disk with filename  |
| :w FILENAME (v) | Saves the visually selected files in file FILENAME  |
| :r FILENAME     | Retrieves disk file FILENAME - put below the cursor |
| :q!             | Quit and discard cchanges                           |
| :w              | Save changes                                        |
| :wq             | Quit and save changes                               |
| :qall           | Quit all                                            |
| :wall           | Save changes among all windows                      |
| :wqall          | Save and quit all windows                           |

### Window navigation

| Command       | Function                                            |
| ------------- | --------------------------------------------------- |
| CTRL-w h      | Move the window to the left                         |
| CTRL-w j      | Move the window to the below                        |
| CTRL-w k      | Move the window to the above                        |
| CTRL-w l      | Move the window to the right                        |
| CTRL-6        | Toggle between buffers                              |
| CTRL-w H      | Move the window to the left                         |
| CTRL-w J      | Move the window to the below                        |
| CTRL-w K      | Move the window to the above                        |
| CTRL-w L      | Move the window to the right                        |
| CTRL-w <      | Decrease the verticalsize of the current window     |
| CTRL-w >      | Increase the verticalsize of the current window     |
| CTRL-w =      | Set sizes equally                                   |
| C-w +         | Inrease the size of a window (horizontal)           |
| C-w -         | Decrease the size of a window                       |
| :split file.c | Opens up file.c in a new window                     |
| :split        | Horizontal split                                    |
| :vsplit       | Verical split                                       |
| :split        | Splits screen two windows. Leaves cursor top window |
| :close        | Closes a window                                     |
| :only         | Closes all window except the one you are in         |
| C-w-w         | Toggle Window                                       |
| C-w C-w       | Jump to other window                                |
| C-L           | Redraw screen                                       |

### Search functionality

| Command         | Function                                              |
| --------------- | ----------------------------------------------------- |
| /what           | Search for the word what in document                  |
| n (search)      | Goes to the next search result (Enter first)          |
| N (search       | Goes to the previous search result (Enter first)      |
| ?what           | Search for the word 'what' in backward direction      |
| C-o (search)    | Go back stepwise from where you searched              |
| `<C-O>`         | Come back to where you came from                      |
| C-L             | Redraws the screen and clears out the marked searches |
| % (n)           | Matching parantheses search                           |
| :s/old/new      | To substitute new for the first old in a line type    |
| :s/old/new/g    | To substitute new for all 'old's on a line type       |
| :#,#s/old/new/g | To substitute phrases between two line #'s type       |
| :%s/old/new/g   | To substitute all occurrences in the file typ         |
| :%s/old/new/gc  | To ask for confirmation each time add 'c'             |
| :%s/png/jpg     | Search and replace word png to jpg                    |
| :noh            | Clear out search highlightning                        |
| `''`            | Takes you back to beginning from where you searched   |

### Buffer navigation

| Command              | Function                              |
| -------------------- | ------------------------------------- |
| :buffers or :ls      | View buffer list                      |
| :buffer 2 (or name)  | Edit buffer 2 (or name)               |
| :sbuffer 3 (or name) | Open buffer 3 in new window (or name) |
| :bnext               | Go to next buffer                     |
| :bprevious           | Go to previous buffer                 |
| :bfirst              | Go to first buffer                    |
| :blast               | Go to last buffer                     |

### Settings

| Command               | Function                                            |
| --------------------- | --------------------------------------------------- |
| :set backup           | Let vim create a backupfile                         |
| :syntax enable        | Enbale syntax highlightning                         |
| :set filetype         | if the filetype is '', type highlightning = unknown |
| :set filetype=fortran | Enable fortran highlighting                         |
| :set background=dark  | Dark background - before enable syntax              |
| :set nackground=light | Light background - set before enable syntax         |

### Other

| Command          | Function                                          |
| ---------------- | ------------------------------------------------- |
| C-g              | Show status of file                               |
| :!ls             | runs the ls command in the shell                  |
| :somecommand C-d | Pops up a completionwindow related to somecommand |
| . (n)            | Repeating commands                                |
| CTRL-Z           | Suspend                                           |
| fg               | Resume                                            |
| :!ls             | Execute the shell command ls                      |

### Folding

| Command | Function             |
| ------- | -------------------- |
| zM      | Close all folds      |
| zR      | Open all folds       |
| zc      | Close a certain fold |
| za      | Open a certain fold  |

### Recording Macro

Example of recording a macro

1. `qc` - record macro `c`.
2. Perform command that you want to put in macro
3. `q` - End macro recording
4. `@c` - perform macro

## Plugins and LSP

### Packer

Please note that there is a lot of options you can pass to packer when you add
a plugin. Please see packers GitHub site for specific options.

### nvim-lua/popup.nvim

An implementation of the Popup API from vim in Neovim.

### Autopairs

An plugin to autopair `(`, `{`, etc.

| Command   | Function                                  |
| --------- | ----------------------------------------- |
| `<ALT-e>` | Insert `(` or `{` and then push `<ALT-e>` |

### Bufferline

Arranges buffers nicely in windows. Please note that there are lot of commands that
you could add to your keymap here.

### vim-bbye - Bbye (Buffer Bye) for Vim

| Command     | Function                                                      |
| ----------- | ------------------------------------------------------------- |
| `:Bdelete`  | Removes file from buffer list, clears options, vars, mappings |
| `:Bwipeout` | Same as above but it also removes file from jumplist `<C-o>`  |

Could be nice to add keymaps for these.

### Lualine

Status line written in lua. Please configure in `lualine.lua` if you deem it necessary.

### Indent-blankline

Lots of configurations that could be done. Please see Github page or `:help indent_blankline.txt`

### hop.nvim

| Command | Function   |
| ------- | ---------- |
| `s`     | `:HopWord` |
| `S`     | `:HopLine` |

### numb.nvim

Peeks lines of the buffer. Just write `:300` to peek line 300

### Zen-mode

Toggle zen-mode with `:ZenMode`

### Neoscroll

Smooth scroll functionality. Works with following commands:

| Command | Function                              |
| ------- | ------------------------------------- |
| `<C-u>` | Moves cursor + screen up half page    |
| `<C-d>` | Moves cursor + screen down half page  |
| `<C-b>` | Moves cursor + screen up 1 page       |
| `<C-f>` | Moves cursor + screen down 1 page     |
| `<C-y>` | Moves screen up 1 line                |
| `<C-e>` | Moves screen down 1 line              |
| `zz`    | Move current line to middle of screen |
| `zt`    | Move current line to top of screen    |
| `zb`    | Move current line to bottom of screen |

### TODO comments

Color highlighting for comments containing: `PERF`, `HACK`, `TODO`, `NOTE`,
`FIX`, `WARNING`

| Command          | Function                                      |
| ---------------- | --------------------------------------------- |
| `:TodoQuickFix`  | Uses the quickfix list to show all todos      |
| `:TodoLocList`   | Uses the locationlist to show all todos       |
| `:TodoTrouble`   | Lists all to do's in `trouble`                |
| `:TodoTelescope` | Search trough all the projects with Telescope |

### Markdown preview

| Command                  | Function                 |
| ------------------------ | ------------------------ |
| `:MarkdownPreviewToggle` | Toggles markdown preview |

### Vim Table Mode

Enter table mode by pressing `<Leader>T` and then use `|` to separate cells.

### nvim/cmp - The completion plugin

A completion engine plugin for neovim written in Lua. Completion sources are
installed from external repositories and "sourced".

### LSP

| Command | Function                            |
| ------- | ----------------------------------- |
| `gD`    | `:lua vim.lsp.buf.declaration()`    |
| `gd`    | `:lua vim.lsp.buf.definition()`     |
| `K`     | `:lua vim.lsp.buf.hover()`          |
| `gi`    | `:lua vim.lsp.buf.implementation()` |
| `<C-K>` | `:lua vim.lsp.buf.signature_help()` |
| `N/A`   | `:lua vim.lsp.buf.rename()`         |
| `gr`    | `:lua vim.lsp.buf.references()`     |
| `N/A`   | `:lua vim.lsp.buf.code_action()`    |

### Nvim-Tree

| Command     | Function                 |
| ----------- | ------------------------ |
| `<Leader>e` | `:NvimTreeToggle`        |
| `a`         | Add file / folder        |
| `r`         | Rename file              |
| `d`         | Delete file              |
| `R`         | Refresh tree             |
| `<C-v>`     | Open in vertical split   |
| `<C-x>`     | Open in horizontal split |
| `<C-t>`     | Open file in new tab     |
| `<TAB>`     | Open file in preview     |

### Null-ls

| Command       | Function                                            |
| ------------- | --------------------------------------------------- |
| `:Format`     | `:lua vim.lsp.buf.formatting_sync()` (Formats file) |
| `NullLspInfo` | See which formatters and linters are attched        |

The formatters are set in the file null-ls.lua in the `lsp` folder.
You might need to adjust `M.on_attach = function(client, bufnr)` function in
the file `handlers.lua` in the `lsp` folder.

### Toggleterm

You can toggle the terminal with the shortcut `<C-\>`. You can also change the
mapping in keymaps.lua In `toggleterm.lua`, you can also specify whether the
window should float, be horizontal or vertical. In this file, you can also
configure functions that define whether `toggleterm` should open a program such
as `python`, `htop`, etc.

You can also specify or map commands such as `:Toggleterm direction=horizontal size=10`.

### Projects

The command `:Telescope projects` lets you search for projects or within
projects. Please note that for javascript projects you should first initiate a
project with `eslint --init` in order for it to work.

### Gitsigns

Adds a color to the left based on whether a part is not committed, deleted etc.

Example of commands:

| Command                  | Function |
| ------------------------ | -------- |
| `:Gitsigns preview_hunk` |          |
| `:Gitsigns next_hunk`    |          |
| `:Gitsigns blame_line`   |          |

### Telescope

Example of commands:

| Command                       | Function                                  |
| ----------------------------- | ----------------------------------------- |
| `Telescope find_files`        | Fuzzy finder                              |
| `Telescope lsp_definitions`   | Same as `gd` i.e. go to definition        |
| `Telescope live_grep`         | Search for text in projects               |
| `Telescope lsp_references`    | As `gr` i.e. shows references to variable |
| `Telescope [] theme=ivy`      | Changes the theme of the window           |
| `Telescope [] theme=dropdown` | Another theme                             |
| `Telescope media_files`       | Shows mediafiles in your project          |

Please note that there are a lot of keybindings to `Telescope`. Please see
`telescope.lua` for more. Please also note that there is different modes for
`Telescope` such as `Normal`, `Insert`, etc.

I think `<Leader>f` is mapped to `:Telescope find_files` and `<Leader>F` to
`:Telescope live_grep`

### Comment

| Command | Function                  |
| ------- | ------------------------- |
| `gcc`   | Comments marked codeblock |

### Compe

The plugin compe has a really useful feature called `Super Tab`. If you for
example enter a code snippet into your code. Cmp will take you to the first
item, for example the function name. After you enter the function name you can
press `<C-e>` and then `<TAB>` and it will take you to the next entry, for
example the first argument in the function.

### Renamer

| Command    | Function                 |
| ---------- | ------------------------ |
| `<F2>` (n) | Rename                   |
| `<F2>` (i) | Rename                   |
| `<c-i>`    | Cursor to start          |
| `<c-a>`    | Set cursor to end        |
| `<c-e>`    | Set cursor to word end   |
| `<c-b>`    | Set cursor to word start |
| `<c-c>`    | Clear line               |
| `<c-u>`    | Undo                     |
| `<c-r>`    | Redo                     |

### Symbols-outline

A tree like view for symbols in Neovim using the Language Server Protocol.

| Command           | Function                                           |
| ----------------- | -------------------------------------------------- |
| `:SymbolsOutline` | Toggles symbols outline                            |
| `<ESC>`           | Close outline                                      |
| `<Enter>`         | Go to symbol location in code                      |
| `<o>`             | Go to symbol location in code without losing focus |
| `<C-SPACE>`       | Hoover current symbol                              |
| `<K>`             | Toggles the current symbol preview                 |
| `<r>`             | Rename symbol                                      |
| `<a>`             | Code actions                                       |
| `<?>`             | Show help message                                  |

### Trouble

| Command              | Function                                              |
| -------------------- | ----------------------------------------------------- |
| `<ESC>`              | Cancel the preview and get back to your last ...      |
| `<q>`                | Close the list                                        |
| `<r>`                | Refresh                                               |
| `<Enter>` or `<TAB>` | Jump to diagnostic or open / close fold               |
| `<C-x>`              | Open buffer in new split                              |
| `<C-v>`              | Open buffer in new vertical split                     |
| `<C-t>`              | Open buffer in new tab                                |
| `<o>`                | Jump to diagnostic and close the list                 |
| `<m>`                | Toggle between workspace and document diagnostic mode |
| `<P>`                | Toggle auto preview                                   |
| `<K>`                | Hoover - Opens a popup with a multiline message       |
| `<p>`                | Preview the diagnostic location                       |
| `<zM>`, `<zm>`       | Close all folds                                       |
| `<zR>`, `<zr>`       | Open all folds                                        |
| `<zA>`, `<za>`       | Toggle fold of current line                           |
| `<k>`                | Previous item                                         |
| `<j>`                | Next item                                             |
