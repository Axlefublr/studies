## Registers

`:reg` - register of deletions

`"` - access the register

`"+` - to access the actual clipboard

`"0` - the last thing just yanked, not deleted

## Writing and saving

`:w path` - write and move the file elsewhere

`:x` - write, but only if there were changes

`ZZ` - same as :x

`ZQ` - same as :q!

## Moving around

`hjkl` - arrow keys

`gj` - treat wrapped line as multiple lines

`gk` - treat wrapped line as multiple lines

`w` - beginning of next word

`W` - the only word separator is whitespace

`e` - end of current word

`E` - the only word separator is whitespace

`b` - beginning of previous word

`B` - the only word separator is whitespace

`gg` - beggining of the file

`G` - end of the file

`ge` - go to the end of the last word

`$` - end of the line

`g$` - treat wrapped line as multiple lines

`0` - start of the line

`g0` - treat wrapped line as multiple lines

`^` - go to the first non-blank character of the line

`g_` - go to the last non-blank character of the line

## Search

`/?` - search forwards / backwards

`n` - go to next search result

`N` - go to prev search result

`#*` - go to next / prev symbol

`gn` - text object of the next match

`gN` - text object of the prev match

`cgn` - change next match

`dgn` - delete next match

`ygn` - yank next match

## Replace

`%` - whole file, not just selection

`s` - substitute

`%s/this/toThis/g` - replace

## Cut, paste, yank

`d` - delete

`dd` - delete the line

`D` - delete the rest of the line

`x` - cut the highlighted character

`X` - cut the character before the highlighted one

`xp` - transpose two characters

`gp / gP` - paste and focus cursor after the text

## g Special commands

`gx` - go to link

`gf` - when focused on a file path, open it

`gd` - go to local declaration

`gD` - go to global declaration

## Jumping

`t` - jump to before symbol after the cursor

`T` - jump to before symbol before the cursor

`f` - jump to on the symbol after the cursor

`F` - jump to on the symbol before the cursor

`;` - repeat the last f/t command forward

`,` - repeat the last f/t command backward

`%` - jump to bracket

`123G / 123gg` - go to absolute line

## Inserting

`i` - insert before the cursor

`I` - insert at the start of the line

`i` - inside

`a` - including what it's inside of

`a` - insert after the cursor

`A` - insert at the end of the line

`s` - insert at instead the character highlighted

`S` - insert at instead the current line

`o` - insert on the next (new) line

`O` - insert on the previous (new) line

`r*` - replace with *

`c` - change

`C` - change until the end of the line

## Visual mode

`v` - visual mode

`V` - select lines

`^v` - column select

`gv` - reselect the last selection

`o` or `O` - move to other end of selection

`vip` - select paragraph

`vap` - select paragraph + outside whitespace

## Marking

`m*` - mark place

`'*` - go to place

`* - go to place, memorized column

`^o` - go back in history

`^i` - go forward in history

`:delm a` - to delete the marker a

`:delm a-z` - all lowercase marks (like regex)

`:noh` - remove highlighting of previous search

## Macros

`q*` - to record a macro

`q` - to then exit

`@*` - to execute a macro

`@@` - execute previous macro

## Scrolling

`H` - go to the top of the screen

`M` - go to the middle of the screen

`L` - go to the bottom of the screen

`zz` - scroll to cursor

`zb` - scroll curr line to bottom

`zt` - scroll curr line to top

`^f` - down a screen

`^b` - up a screen

`^d` - down half a screen

`^u` - up half a screen

## Formatting

`J` - joins lines with a space in between

`gJ` - joins lines without a space in between

`gq` - format a wrapped line to be multiple lines

## Capitalization

`gu` - uncapitalize

`gU` - capitalize

`~` - switch capitalization of the highlighted char

`g~` - switch, but you give a text object to it

## Undo, redo, do again

`.` - repeat last command

`u` - undo

`U` - undo the line to the state it was in when the cursor was moved to it

`^r` - redo

## Indenting

`<< >>` - indent / outdent line

`==` - autoindent

## Go to

`(` - go to the last sentence

`)` - go to the prev sentence

`-` - go to first non-whitespace of previous line

`+` - go to first non-whitespace of next line

`[` - go to previous {} section

`]` - go to next {} section

`{` - go to prev blank line

`}` - go to next blank line

## Surround plugin

`ys` - surround the text object with a char

`cs` - change *this* character to *that* character (while inside of them)

`ds` - remove *this* wrapping

`S` - wrap when in visual mode

## Vs code special

`gh` - show hover tooltip

## Commands

`:vs` - split current editor to the right

`:sp` - split current editor down