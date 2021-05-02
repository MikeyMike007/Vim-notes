# VIM notes

## Commands relating to window navigations

| Command               | Description                                          |
|-----------------------|------------------------------------------------------|
| hjkl                  | Move cursor left, down, up, right                    |
| 2w (normal)           | Cursor two words forward                             |
| 3e (normal)           | Cursor to the end of the third word forward          |
| 0 (normal)            | Cursor to the beginning of line                      |
| d2w (nornal)          | Delete 2 words                                       |
| dd (n)                | Delete whole line                                    |
| $ (n)                 | Move to end end of the line                          |
| 2dd (n)               | Delete twp lines                                     |
| u (n)                 | Undo                                                 |
| U  (n)                | Undo all edits on a row                              |
| p (n)                 | Put on line below                                    |
| rx (n)                | Replace the character under the cursor with 'x'      |
| ce (n)                | Delete rest of the word  under and right to cursor   |
| :%s/png/jpg           | Search and replace word png to jpg                   |
| u (normal)            | Undo change                                          |
| x (normal)            | Delete character under cursor                        |
| A (normal)            | Append text at the end of the line                   |
| dw (normal)           | Delete a word                                        |
| d$                    | Delete the rest of the line - right to the cursor    |
| d                     | Delete operator                                      |
| dw                    | Delete a word, excluding itd first character         |
| de                    | Delete a word, including the last character          |
| C-r                   | Redo                                                 |
| c$                    | Delete the rest of the line right from cursor        |
| C-g                   | Show status of file                                  |
| :!ls                  | runs the ls command in the shell                     |
| o (n)                 | Opens up a line below                                |
| O (n)                 | Opens up a line abov                                 |
| a (n)                 | Appends text after cursor                            |
| A (n)                 | Appends text at the end of the current line          |
| e (n)                 | Jump to the end of the word / next word              |
| w (n)                 | Jump to the start of the word / next word            |
| j$                    | Put the cursor at the end of next line               |
| y (v)                 | Enter visual model and select text, copy text with y |
| :somecommand C-d      | Pops up a completionwindow related to somecommand    |
| C-w C-w               | Jump to other window                                 |
| J                     | Joins the current line with the line below           |
| 4x (n)                | Deletes 4 characters                                 |
| d4w (n)               | Deletes 4 words                                      |
| d4e (n)               | Deletes 4 words                                      |
| d$                    | Deletes the rest of the line                         |
| x = dl (n)            | Delete character under the cursor                    |
| X = dh (n)            | Delete character left of the cursor                  |
| D = d$ (n)            | Delete to end of the line                            |
| C = c$ (n)            | Change to end of the line                            |
| s = cl (n)            | Change one character                                 |
| S = cc (n)            | Change the whole line                                |
| . (n)                 | Repeating commands                                   |
| jk (v)                | Select lines up or down in visual mode               |
| cw                    | Change the underlying word                           |
| dw then p             | When you delete, text is saved. Use p for put back   |
| P                     | Put before cursor                                    |
| p                     | Put after cursor                                     |
| y                     | yank character                                       |
| yw                    | yank word                                            |
| y3w                   | Yank three words                                     |
| yy                    | Yanks whole line                                     |
| daw                   | Delete a word (irrespective where cursor is)         |
| dG                    | Delete until the end of line                         |
| dgg                   | Delete until the start of line                       |
| :set backup           | Let vim create a backupfile                          |
| :syntax enable        | Enbale syntax highlightning                          |
| :set filetype         | if the filetype is '', type highlightning = unknown  |
| :set filetype=fortran | Enable fortran highlighting                          |
| :set background=dark  | Dark background - before enable syntax               |
| :set nackground=light | Light background - set before enable syntax          |
| C-w-w                 | Toggle Window                                        |
| :colorscheme x        | Sets the colorscheme x                               |
| :split                | Splits screen two windows. Leaves cursor top window  |
| :close                | Closes a window                                      |
| :only                 | Closes all window except the one you are in          |
| z ENTER               | Move current line to top of screen and scroll        |
| z.                    | Move current line t center of screen and scroll      |
| z-                    | Move current line to bottom of screen and scroll     |
| C-L                   | Redraw screen                                        |
| ``                    | Return to previous mark or context                   |
| ''                    | Return to beginning og line containing previous mark |
| CTRL-v shift I        | Enter text in block mode                             |
| CTRL-Z                | Suspend                                              |
| fg                    | Resume                                               |
| :!ls                  | Execute the shell command ls                         |
| d (v)                 | Cut text                                             |
| dd (v)                | Cut whole line                                       |
| ciw                   | Delete a word and insert                             |
| yaw                   | Yank a word                                          |
| CTRL-V                | Paste from clipboard                                 |

## Modes

| Esc   | Normal mode                                     |
| Esc-i | Insert mode (Text will be inserted after cursor |
| C-v   | Start visual block modes                        |
| Esc-R | Enters replace mode. Overwrites under cursor    |

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

| Command       | Function                                        |
|---------------|-------------------------------------------------|
| CTRL-w h      | Move the window to  the left                    |
| CTRL-w j      | Move the window to  the below                   |
| CTRL-w k      | Move the window to  the above                   |
| CTRL-w l      | Move the window to  the right                   |
| CTRL-6        | Toggle between buffers                          |
| CTRL-w H      | Move the window to  the left                    |
| CTRL-w J      | Move the window to  the below                   |
| CTRL-w K      | Move the window to  the above                   |
| CTRL-w L      | Move the window to  the right                   |
| CTRL-w <      | Decrease the verticalsize of the current window |
| CTRL-w >      | Increase the verticalsize of the current window |
| CTRL-w =      | Set sizes equally                               |
| C-w +         | Inrease the size of a window (horizontal)       |
| C-w -         | Decrease the size of a window                   |
| :split file.c | Opens up file.c in a new window                 |
| :split        | Horizontal split                                |
| :vsplit       | Verical split                                   |
| C-F           | Scroll forward one screen                       |
| C-B           | Scroll backward one screen                      |
| C-D           | Scroll forward half screen                      |
| C-U           | Scroll backward half screen                     |
| G (n)         | Move cursor to EOF                              |
| gg (n)        | Move cursor to top of file                      |
| H             | Move to home - the top line of screen           |
| M             | Move to middle of screen                        |
| L             | Move to bottom line of screen                   |
| Enter         | Move to first character of next line            |
| nG            | Go to given line n                              |

## Search functionality

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

## Other useful stuff

### FILE MARKS

In chapter 4 was explained how you can place a mark in a file with "mx" and
jump to that position with "`x".  That works within one file.  If you edit
another file and place marks there, these are specific for that file.  Thus
each file has its own set of marks, they are local to the file.
So far we were using marks with a lowercase letter.  There are also marks
with an uppercase letter.  These are global, they can be used from any file.
For example suppose that we are editing the file "foo.txt".  Go to halfway
down the file ("50%") and place the F mark there (F for foo): >

   50%mF

Now edit the file "bar.txt" and place the B mark (B for bar) at its last line:
  
  GmB

Now you can use the "'F" command to jump back to halfway of foo.txt.  Or edit
yet another file, type "'B" and you jump to the end of bar.txt.

The file marks are remembered until they are placed somewhere else.  Thus you
can place the mark, do hours of editing and still be able to jump back to that
mark.

It's often useful to think of a simple connection between the mark letter
and where it is placed.  For example, use the H mark in a header file, M in
a Makefile and C in a C code file.

To see where a specific mark is, give an argument to the ":marks" command: >

:marks M

You can also give several arguments: >

:marks MCP

Don't forget that you can use CTRL-O and CTRL-I to jump to older and newer
positions without placing marks there.


















## Other handy commands

| Command                   | Description                                  |
|---------------------------|----------------------------------------------|
| mogrify -format jpg *.png | Converts all png files to jpg in a directory |



