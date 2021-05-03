# VIM notes

Following document illustrates my most used vim commands.

## Modes

| Command    | Function                                      |
|------------|-----------------------------------------------|
| Esc        | Normal mode                                   |
| Esc-i      | Insert mode                                   |
| Esc-v      | Visual mode                                   |
| Esc-V      | Visual row mode                               |
| Esc-CTRL-v | Visual block mode                             |
| Esc-R      | Enters replace mode (Overwrites under cursor) |

## Cursor movements

| Command | Function                                         |
|---------|--------------------------------------------------|
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

## Edit

| Command        | Function                                                |
|----------------|---------------------------------------------------------|
| i              | Inserts text at the left to cursor                      |
| a              | Inserts text at the right to cursor                     |
| I              | Insert at the start of the current line                 |
| A              | Insert at the end of the current line                   |
| o              | Insert a line below current line                        |
| O              | Insert a line above the current line                    |
| s (cl)         | Delete character under cursor and start insert          |
| S  (cc)        | Delete all text on line and start insert at beg of line |
| C (c$)         | Delete everything right to the cursor and insert        |
| cw             | Delete to the end of word and start inserting           |
| ce             | Delete rest of the word under and right to cursor       |
| ciw            | Delete a word and insert                                |
| rx             | Replace the character under the cursor with 'x'         |
| u              | Undo                                                    |
| U              | Undo all edits on a row                                 |
| CTRL-r         | Redo                                                    |
| J              | Joins the current line with the line below              |
| CTRL-v shift I | Enter text in block mode                                |

## Cut, copy and paste

| Command | Function                               |
|---------|----------------------------------------|
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

## Deletion

| Command | Function                                          |
|---------|---------------------------------------------------|
| d       | Delete operator                                   |
| dw      | Delete a word (cursor needs to be at beg of word) |
| de      | Delete a word                                     |
| daw     | Delete a word (irrespective where cursor is)      |
| d2w     | Delete 2 words                                    |
| d4w (n) | Deletes 4 words                                   |
| d4e (n) | Deletes 4 words                                   |
| dd (n)  | Delete whole line                                 |
| 2dd (n) | Delete two lines                                  |
| d$      | Delete the rest of the line - right of the cursor |
| c$      | Delete the rest of the line right from cursor     |
| D (d$)  | Delete to end of the line                         |
| x (dl)  | Delete character under the cursor                 |
| 4x      | Deletes 4 characters                              |
| X (dh)  | Delete character left of the cursor               |
| dG        | Delete until the end of line                       |
| dgg       | Delete until the start of line                     |
| dw then p | When you delete, text is saved. Use p for put back |

## Working with files

| Command         | Function                                            |
|-----------------|-----------------------------------------------------|
| :w FILENAME     | Writes the currrent vim file to disk with filename  |
| :w FILENAME (v) | Saves the visually selected files in file FILENAME  |
| :r FILENAME     | Retrieves disk file FILENAME - put below the cursor |
| :q!             | Quit and discard cchanges                           |
| :w              | Save changes                                        |
| :wq             | Quit and save changes                               |
| :qall           | Quit all                                            |
| :wall           | Save changes among all windows                      |
| :wqall          | Save and quit all windows                           |

## Window navigation

| Command       | Function                                            |
|---------------|-----------------------------------------------------|
| CTRL-w h      | Move the window to  the left                        |
| CTRL-w j      | Move the window to  the below                       |
| CTRL-w k      | Move the window to  the above                       |
| CTRL-w l      | Move the window to  the right                       |
| CTRL-6        | Toggle between buffers                              |
| CTRL-w H      | Move the window to  the left                        |
| CTRL-w J      | Move the window to  the below                       |
| CTRL-w K      | Move the window to  the above                       |
| CTRL-w L      | Move the window to  the right                       |
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

## Search functionality

| Command         | Function                                              |
|-----------------|-------------------------------------------------------|
| /what           | Search for the word what in document                  |
| n (search)      | Goes to the next search result                        |
| N (search       | Goes to the previous search result                    |
| ?what           | Search for the word 'what' in backward direction      |
| C-o (search)    | Go back stepwise from where you searched              |
| C-L             | Redraws the screen and clears out the marked searches |
| % (n)           | Matching parantheses search                           |
| :s/old/new      | To substitute new for the first old in a line type    |
| :s/old/new/g    | To substitute new for all 'old's on a line type       |
| :#,#s/old/new/g | To substitute phrases between two line #'s type       |
| :%s/old/new/g   | To substitute all occurrences in the file typ         |
| :%s/old/new/gc  | To ask for confirmation each time add 'c'             |
| :%s/png/jpg     | Search and replace word png to jpg                    |

## Buffer navigation

| Command              | Function                              |
|----------------------|---------------------------------------|
| :buffers or :ls      | View buffer list                      |
| :buffer 2 (or name)  | Edit buffer 2 (or name)               |
| :sbuffer 3 (or name) | Open buffer 3 in new window (or name) |
| :bnext               | Go to next buffer                     |
| :bprevious           | Go to previous buffer                 |
| :bfirst              | Go to first buffer                    |
| :blast               | Go to last buffer                     |

## Settings

| Command               | Function                                            |
|-----------------------|-----------------------------------------------------|
| :set backup           | Let vim create a backupfile                         |
| :syntax enable        | Enbale syntax highlightning                         |
| :set filetype         | if the filetype is '', type highlightning = unknown |
| :set filetype=fortran | Enable fortran highlighting                         |
| :set background=dark  | Dark background - before enable syntax              |
| :set nackground=light | Light background - set before enable syntax         |

## Working with marks

| Command | Function                                             |
|---------|------------------------------------------------------|
| ``      | Return to previous mark or context                   |
| ''      | Return to beginning og line containing previous mark |

## Other

| Command          | Function                                          |
|------------------|---------------------------------------------------|
| C-g              | Show status of file                               |
| :!ls             | runs the ls command in the shell                  |
| :somecommand C-d | Pops up a completionwindow related to somecommand |
| . (n)            | Repeating commands                                |
| CTRL-Z           | Suspend                                           |
| fg               | Resume                                            |
| :!ls             | Execute the shell command ls                      |

## Other non-vim handy commands

| Command                   | Function
|---------------------------|----------------------------------------------|
| mogrify -format jpg *.png | Converts all png files to jpg in a directory |

