## Allocate a console to a process

https://learn.microsoft.com/en-us/windows/console/allocconsole

[The ahk library for it](https://github.com/Onimuru/Console) (v2 beta 9)

## Change display brightness

[gist](https://gist.github.com/TLMcode/b56c71ef4785f1ef8daada9c36a38db4)

## Playing multiple sounds at a time

[docs](https://learn.microsoft.com/en-us/windows/win32/multimedia/the-playsound-function)

## Clickthrough

`+E0x20`

Makes a gui clickthrough, but also requires

`WinSetTransparent(255, guiWinTitle)`

## Gui doesn't appear in taskbar

`+ToolWindow`

Even though it's a plus, it really means -

## Make the gui think you clicked on the title bar

`PostMessage(0xA1, 2)`

## @things the v2 extension supports

* exception
* extends
* lends
* interments
* modifies
* private
* protected
* returns?
* throws
* type
* example - Use the `<caption>` tag to give a caption (recommended). Everything after is code