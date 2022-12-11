## Resouces

[vimscript to lua](https://vonheikemen.github.io/devlog/tools/configuring-neovim-using-lua/)

[vimscript to lua2](https://vonheikemen.github.io/devlog/tools/build-your-first-lua-config-for-neovim/)

[key codes](https://github.com/neovim/neovim/blob/b535575acdb037c35a9b688bc2d8adc2f3dece8d/src/nvim/keymap.h#L225)

[person comment that suggested key codes](https://www.reddit.com/r/neovim/comments/kup1g0/comment/givujwd/?utm_source=share&utm_medium=web2x&context=3)

## Settings

`vim.o`  - general setttings

`vim.wo` - window scoped settings

`vim.bo` - buffer scoped settings

`vim.g`  - global settings

`vim.env` - environment settings

`vim.opt` - works for setting pretty much anything

## Accessing the unaccessible

`vim.fn` - calls a vim function

`vim.call` - same thing, but you provide the name of the function as a string