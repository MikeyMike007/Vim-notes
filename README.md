# VIM notes

## Commands relating to window navigations

| Command      | Description                                               |
|--------------|-----------------------------------------------------------|
| hjkl         | Move cursor left, down, up, right                         |
| Esc          | Normal mode                                               |
| C-6          | Toggle between buffers                                    |
| C-w hjkl     | Move around between split windows                         |
| K            | Open link in new buffer                                   |
| Esc-i        | Insert mode (Text will be inserted after cursor           |
| 2w (normal)  | Cursor two words forward                                  |
| 3e (normal)  | Cursor to the end of the third word forward               |
| 0 (normal)   | Cursor to the beginning of line                           |
| d2w (nornal) | Delete 2 words                                            |
| dd (n)       | Delete whole line                                         |
| $ (n)        | Move to end end of the line                               |
| 2dd (n)      | Delete twp lines                                          |
| u (n)        | Undo                                                      |
| U  (n)       | Undo all edits on a row                                   |
| p (n)        | Put on line below                                         |
| rx (n)       | Replace the character under the cursor with 'x'           |
| ce (n)       | Delete rest of the word  under and to the right to cursor |
| :%s/png/jpg  | Search and replace word png to jpg                        |
| u (normal)   | Undo change                                               |
| :q!          | Quit and discard cchanges                                 |
| :w           | Save changes                                              |
| :wq          | Quit and save changes                                     |
| x (normal)   | Delete character under cursor                             |
| A (normal)   | Append text at the end of the line                        |
| dw (normal)  | Delete a word                                             |
| d$           | Delete the rest of the line which is right to the cursor  |
| d            | Delete operator                                           |
| dw           | Delete a word, excluding itd first character              |
| de           | Delete a word, including the last character               |

## Other handy commands

| Command                   | Description                                  |
|---------------------------|----------------------------------------------|
| mogrify -format jpg *.png | Converts all png files to jpg in a directory |
