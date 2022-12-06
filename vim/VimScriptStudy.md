## `<Cmd>`

```vim
:command<CR>
<Cmd>command<CR>
```

The latter is more performant and doesn't change modes

However, it doesn't support recursive remaps

## Functions

`repeat(expr, count)` concatenates the expression `count` times

`feedkeys(string, [mode])` puts string as keys into the typeahead buffer. use the 'i' flag for
typebefore

`"\<CR>"` presses Enter, `'\<CR>'` sends the keys literally

`getline('.')` gets the current line

## Built-in vim variables

`v:count1` the count given for the last Normal mode command
