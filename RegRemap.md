## How to remap keys in the registry!

### Creating the scancode map

Press Windows + R and type in `regedit`

Windows will ask for your admin permission, press yes and go to:

`Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Keyboard Layout`

Right click to create a new binary value: Scancode Map

### Filling the scancode map

First line is filled with zeros, until the next line (16 zeros to be precise)

After that, `02 00 00 00` is the header, where 02 means "one remap"

As you have more and more remaps, you increase that number

I think it uses hex, so base 16 rather than base 10

You only need to change the first number, the 6 zeros after stay the same way

Now comes the actual remap

`1C 00 3A 00` where 1C00 is enter and 3A00 is capslock => remapping capslock *to* enter

`00 00 00 00` at the end of the map: there was a header, well this is the "bottomer"

### Available key codes

|    Key name | Hex key code |
|    -------- | ------------ |
|         Esc | 0100         |
|          1! | 0200         |
|          2@ | 0300         |
|          3# | 0400         |
|          4$ | 0500         |
|          5% | 0600         |
|          6^ | 0700         |
|          7& | 0800         |
|          8* | 0900         |
|          9( | 0A00         |
|          0) | 0B00         |
|          -_ | 0C00         |
|          =+ | 0D00         |
|   Backspace | 0E00         |
|         Tab | 0F00         |
|           q | 1000         |
|           w | 1100         |
|           e | 1200         |
|           r | 1300         |
|           t | 1400         |
|           y | 1500         |
|           u | 1600         |
|           i | 1700         |
|           o | 1800         |
|           p | 1900         |
|         \[{ | 1A00         |
|          ]} | 1B00         |
|       Enter | 1C00         |
|        Ctrl | 1D00         |
|           a | 1E00         |
|           s | 1F00         |
|           d | 2000         |
|           f | 2100         |
|           g | 2200         |
|           h | 2300         |
|           j | 2400         |
|           k | 2500         |
|           l | 2600         |
|          ;: | 2700         |
|          '" | 2800         |
|          `~ | 2900         |
|  Left Shift | 2A00         |
|         \\\|| 2B00         |
|           z | 2C00         |
|           x | 2D00         |
|           c | 2E00         |
|           v | 2F00         |
|           b | 3000         |
|           n | 3100         |
|           m | 3200         |
|          ,< | 3300         |
|          .> | 3400         |
|          /? | 3500         |
| Right shift | 3600         |
| Printscreen | 3700         |
|         Alt | 3800         |
|       Space | 3900         |
|    Capslock | 3A00         |
|          F1 | 3B00         |
|          F2 | 3C00         |
|          F3 | 3D00         |
|          F4 | 3E00         |
|          F5 | 3F00         |
|          F6 | 4000         |
|          F7 | 4100         |
|          F8 | 4200         |
|          F9 | 4300         |
|         F10 | 4400         |
|         F11 | 57E0         |
|         F12 | 58E0         |
|     Numlock | 4500         |
|  ScrollLock | 4600         |
|        Home | 4700         |
|          Up | 4800         |
|        PgUp | 3900         |
|        Left | 4B00         |
|       Right | 4D00         |
|         End | 4F00         |
|        Down | 5000         |
|        PgDn | 5100         |
|      Insert | 5200         |
|      Delete | 5300         |

### Additional information

If a remap doesn't work, try changing the `00` at the end to a `E0` and try again

Don't forget to reboot your computer for the changes to start working!

[site with keycodes I might've missed](https://www.technewstoday.com/how-to-remap-keyboard-keys/)
