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

* extends
* modifies
* private
* protected
* returns?
* throws
* type
* example - Use the `<caption>` tag to give a caption (recommended). Everything after is code
    
## Open waveaudio

```javascript
new SoundBoard("zoom", "C:\Users\***\Music\zoom.wav", "Numpad1")
new SoundBoard("boxout", "C:\Users\***\Music\boxout.wav", "Numpad2")
new SoundBoard("test", "C:\Users\***\Music\test.mp3", "Numpad3")

class SoundBoard {
   __New(alias, path, key) {
      this.alias := alias ;unused
      this.path := path
      this.key := key
      this.ext := this.GetExt()
      this.Register()
   }
   GetExt() {
      SplitPath, % this.path,,,ext
      return ext
   }
   mciSend(command) {
      DllCall("winmm\mciSendStringW", "Str", command, "Str", "", "UInt", 0, "Ptr", 0)
   }
   Register() {
      static map := {"mp3": "waveaudio", "wav": "waveaudio"}
      this.boundObj := ObjBindMethod(this, "Play")
      temp := this.boundObj
      Hotkey, % this.key, % temp
      this.mciSend(Format("open {1} type {2}", this.path, map[this.ext]))
   }
   Play() {
      this.mciSend("play " this.path " from 0")
   }
}
```

[multimedia command strings](https://learn.microsoft.com/en-us/windows/win32/multimedia/multimedia-command-strings?redirectedfrom=MSDN)