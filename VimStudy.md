### `:reg` - register of deletions

" - access the register

"+ - to access the actual clipboard

"o - the last thing just yanked, not deleted

### !sort - sorts selected lines

### :w path - write and move the file elsewhere

### hjkl - arrow keys

### gj - treat wrapped line as multiple lines

### gk - treat wrapped line as multiple lines

### replace

% - whole file, not just selection

s - substitute

`%s/this/toThis/g` - replace

#### g& - run last replace globally

### w - beginning of next word

### W - the only word separator is whitespace

### e - end of current word

### E - the only word separator is whitespace

### b - beginning of previous word

### B - the only word separator is whitespace

### d - delete

### dd - delete the line

### D - delete the rest of the line

gx - go to link

gf - when focused on a file path, open it

gg - beggining of the file

G - end of the file

ge - go to the end of the last word

gd - go to local declaration

gD - go to global declaration

### t - jump to before symbol after the cursor

### T - jump to before symbol before the cursor

### f - jump to on the symbol after the cursor

### F - jump to on the symbol before the cursor

### ; - repeat the last f/t command forward

### , - repeat the last f/t command backward

### i - insert before the cursor

### I - insert at the start of the line

i - inside

### a - insert after the cursor

### A - insert at the end of the line

### s - insert at instead the character highlighted

### S - insert at instead the current line

### / - search

n - go to next search result

N - go to previous search result

? - search backwards

\# * - go to next / prev symbol

### v - visual mode

V - select lines

^v - column select

gv - reselect the last selection

### o - insert on the next (new) line

O - insert on the previous (new) line

### m* - mark place

'* - go to place

### q* - to record a macro

q - to then exit

### Moving

H - go to the top of the screen

M - go to the middle of the screen

L - go to the bottom of the screen

\$ - end of the line

g$ - treat wrapped line as multiple lines

0 - start of the line

g0 - treat wrapped line as multiple lines

^ - go to the first non-blank character of the line

g_ - go to the last non-blank character of the line

### Joining / unwrapping lines

J - joins lines with a space in between

gJ - joins lines without a space in between

gq - format a wrapped line to be multiple lines

### Capitalization

gu - uncapitalize

gU - capitalize

~ - switch capitalization of the highlighted char

g~ - switch, but you give a text object to it

### x - cut the highlighted character

xp - transpose two characters

### ^o - go back in history

^i - go forward in history

### :r! command

pastes the output of the command

@* - to execute a macro

. - repeat last command

u - undo

^r - redo

r - replace with |.|

c - change

% - jump to bracket

123G / 123gg - go to absolute line

<< >> - indent / outdent line

== - autoindent

zz - scroll to cursor