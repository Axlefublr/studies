`#variable` - gets the length of the string

`type(variable)` - gets the type of a variable 

(number, boolean, nil)

Floats can have up to 13 digits after the dot

```lua
string = [[
   this is how string continuation is done
]]
```

`..` for concatenation

`nil`, not null

`~=`, not `!=`

words instead of ! && ||

`elseif`, not `else if`

## Strings

`string.len`, not `.Length`

`string.gsub` = `StrReplace`

`string.find` - finds the first index of a search you put in

`string.upper`, `string.lower`

`string.gmatch(string, regex)` 

---

```lua
repeat
   code
until condition
```

```lua
for i = 0, 10, 1 do
end
```

until the value of i is 10

increment by 1

```lua
for key, value in pairs(table) do
end
```

`table.insert(table, index, value)`

`table.remove(table, index)`

`table.concat(table, concatSymbol)` - converts to a string

Functions can return multiple values

Variadic parameters are `...`

Has coroutines

## Working with files

* r - read only
* w - write or overwrite
* a - write or append
* r+ - read and write
* w+ - overwrite, read, or create
* a+ - append, read, or create
    
`io.open` creates the file object

Methods are used via `:`

`fileObj:write(text)`

`fileObj:seek(seekOpt, index)` - "set" for seekOpt to set the cursor to there

`fileObj:close()` 

`fileObj:read("*a")` - read everything

## Modules

Create a local module variable

Stuff that will be inside of the module now has to start with the variable name + a dot, then the name of the thing

return the module variable

require it in the other file to use it