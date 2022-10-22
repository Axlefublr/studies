## Clickthrough

`+E0x20`

Makes a gui clickthrough, but also requires

`WinSetTransparent(255, guiWinTitle)`

## Gui doesn't appear in taskbar

`+ToolWindow`

Even though it's a plus, it really means -

## Make the gui think you clicked on the title bar

`PostMessage(0xA1, 2)`