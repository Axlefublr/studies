## General rules

A key typed twice affects the whole line

## Keys

hjkl - arrow keys

## Commands

### replace

% - whole file, not just selection

s - substitute

`%s/this/toThis/g` - replace

## `:reg` - register of deletions

" - access the register

"+ - to access the actual clipboard

"o - the last thing just yanked, not deleted

### w - beginning of next word

W - the only word separator is whitespace

### e - end of current word

E - the only word separator is whitespace

### b - beginning of previous word

B - the only word separator is whitespace

### d - delete

dd - delete the line

D - delete the rest of the line

### g - go

gg - beggining of the file

G - end of the file

ge - go to the end of the last word

gd - go to local declaration

gD - go to global declaration

### t - jump to before symbol after the cursor

T - jump to before symbol before the cursor

### f - jump to on the symbol after the cursor

F - jump to on the symbol before the cursor

### i - insert before the cursor

I - insert at the start of the line

i - inside

### a - insert after the cursor

A - insert at the end of the line

### / - search

n - go to next search result

N - go to previous search result

? - search backwards

\# * - go to next / prev symbol

### v - visual mode

V - select lines

^v - column select

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

0 - start of the line

^ - go to the first non-blank character of the line

g_ - go to the last non-blank character of the line

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