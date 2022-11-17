## Registers

`:reg` - register of deletions

`"` - access the register

`"+` - to access the actual clipboard

`"0` - the last thing just yanked, not deleted

`_` - black hole register

`-` - last less than a line yank / delete

### Registers: custom

`i` - black hole register

`q` - system clipboard

`w` - last yank clipboard

`e` - last less than a line yank / delete

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

### Moving around: custom made

`zj` - move to previous folding section

`zk` - move to next folding section

`[c ]c` - go to prev / next change

`[e ]e` - go to prev / next error

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

`zd` - delete everything on the line, but keep the line itself

`x` - cut the highlighted character

`X` - cut the character before the highlighted one

`xp` - transpose two characters

`gp / gP` - paste and focus cursor after the text

## g Special commands

`gx` - go to link

`gf` - when focused on a file path, open it

`gd` - go to local declaration

`gD` - go to global declaration

### g Special commands: custom and vscode

`gl` - go to link

`gD` - open definition to the side

## Jumping

`t` - jump to before symbol after the cursor

`T` - jump to before symbol before the cursor

`f` - jump to on the symbol after the cursor

`F` - jump to on the symbol before the cursor

`;` - repeat the last f/t command forward

`,` - repeat the last f/t command backward

`%` - jump to bracket

`123G / 123gg` - go to absolute line

`gi` - insert at the last place you inserted at

`10i` - insert text *this* many times

## Inserting

`i` - insert before the cursor

`I` - insert at the start of the line

`gi` - insert at the last insertion position

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

`Ctrl + a` - paste text last inserted in insert mode

`Ctrl + o` - do one command in normal mode and come back

`Ctrl + u` - delete line

`Ctrl + r =` - evaluate an expression and paste its result

## Visual mode

`v` - visual mode

`V` - select lines

`^v` - column select

`gv` - reselect the last selection

`o` or `O` - move to other end of selection

`vip` - select paragraph

`vap` - select paragraph + outside whitespace

`'<` - start of the selection

`'>` - end of the selection

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

`=` - format a text object

`<< >>` - indent / outdent line

`==` - autoindent

`Ctrl d / t` - indent / outdent line (in insert mode)

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

## Go to

`(` - go to the last sentence

`)` - go to the prev sentence

`-` - go to first non-whitespace of previous line

`+` - go to first non-whitespace of next line

`{` - go to prev blank line

`}` - go to next blank line

## Surround plugin

`ys` - surround the text object with a char

`cs` - change *this* character to *that* character (while inside of them)

`ds` - remove *this* wrapping

`S` - wrap when in visual mode

## Vs code special

`gh / K` - show hover tooltip

`mi / ma` - multiple cursors when in selection mode

Calling a vscode function via a remap:

```vim
<Cmd>call VSCodeNotify('vscode.command')<CR>
```
| Command                                                                                                                                                           | Description                                                                                                                                                                                                |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `VSCodeNotify(command, ...)` <br/> `VSCodeCall(command, ...)`                                                                                                     | Invoke VSCode command with optional arguments.                                                                                                                                                             |
| `VSCodeNotifyRange(command, line1, line2, leaveSelection ,...)` <br/> `VSCodeCallRange(command, line1, line2, leaveSelection, ...)`                               | Produce linewise VSCode selection from `line1` to `line2` and invoke VSCode command. Setting `leaveSelection` to 1 keeps VSCode selection active after invoking the command.                               |
| `VSCodeNotifyRangePos(command, line1, line2, pos1, pos2, leaveSelection ,...)` <br/> `VSCodeCallRangePos(command, line1, line2, pos1, pos2, leaveSelection, ...)` | Produce characterwise VSCode selection from `line1.pos1` to `line2.pos2` and invoke VSCode command.                                                                                                        |
| `VSCodeNotifyVisual(command, leaveSelection, ...)` <br/> `VSCodeCallVisual(command, leaveSelection, ...)`                                                         | Produce linewise (visual line) or characterwise (visual and visual block) selection from visual mode selection and invoke VSCode command. Behaves like `VSCodeNotify/Call` when visual mode is not active. |

## Mapping

`map` - is recursive, will be used in other remaps

`noremap` - is not recursive, if you refer to the remapee, its initial function will work instead of the one you made

You can specify letters before `map` / `noremap` / `unmap` (but only one per remap)

* n - Normal
* v - Visual and Select
* s - Select
* x - Visual
* o - Operator pending
* ! - Insert and Command-Line (after the keyword instead of before)
* i - Insert
* l - Insert, Command-Line and Lang-Arg
* c - Command-Line
* t - Terminal-Job

With no specification: Normal, Visual, Select, Operator pending

There can be special arguments to remaps

* `<buffer>`
* `<nowait>`
* `<silent>` - Prevents echoing of the command
* `<special>`
* `<script>`
* `<expr>`
* `<unique>`

This is the syntax:

```
map <special-argument> key-trigger key-sequence
```

## Folding

`za` - toggle fold

`zC` - fold every section

`zO` - unfold every section

## Text objects

`s` - sentence

## VimScript

### `<Cmd>`

```vim
:command<CR>
<Cmd>command<CR>
```

The latter is more performant and doesn't change modes

However, it doesn't support recursive remaps

### Functions

`repeat(expr, count)` concatenates the expression `count` times

`feedkeys(string, [mode])` puts string as keys into the typeahead buffer. use the 'i' flag for
typebefore

`"\<CR>"` presses Enter, `'\<CR>'` sends the keys literally

`getline('.')` gets the current line

### Built-in vim variables

`v:count1` the count given for the last Normal mode command