## Variables

```sh
name="value"
$name
```

## Reading the output of a command as a variable

`name=$(read)` Instead of reading a variable, we're reading the output of a command

You don't have to assign it to a variable, you can do it inline too

`echo "you are $(whoami), currently in the $(pwd) directory"` => you are axlefublr, currently in the /home/axlefublr directory

## Processing user input

`read variable` Meaning, "read into variable"

## Passing parameters to a script

Pass parameters after the path just like in bat

When accessing, use `$1`, `$2`, etc, just like bat

## If statements and comparison

```bash
if [ $name == "Sergey" ]; then
   echo your name is $name
else
   echo your name is not $name
fi
```

There *have* to be `[]` with spaces between them

## Useful commands

`whoami` to get the current user echoed

`pwd` print current working directory

`date` print current date and time

`grep -i "to search for" file.txt` find lines that contain "to search for" in the file

`du -h file.txt` check how big a file is

`chown diff-user file.txt` change ownership of a file

`chmod +x -r +w filepath` change permissions for a file

`reset` reset your shell (like restart)

`htop` system info program

`top` see the top processes

`find` to find a file `-name` for the name you provide

`whatis` a more human quick explanation of a command

`man` for an actual manual

`whereis` to check where the command executable lies 

`truncate -s size-int file.txt` deletes the contents of a file, without deleting the file itself

## Cool commands

`sort` sorts a file's contents alphabetically

`shred` tear up the contents of a file without deleting it

`ping` check connection to a website

`neofetch` you might have to install this one. shows system information

`cal`

`cmatrix`

`tail -f file.txt` watch as the file is filled in real time

## Jumping between directories

`pushd /Programming` stash a directory to come back later to

`popd` come back to it

`cd -` go back to the directory you were just in (not necessarily the upper dir)

`.` refers to the current directory

`..` refers to the previous directory

`/` - root

`~` - home directory

## Special symbols

`!!` refers to the last command executed

If you forgot that the command needed sudo, you can just do `sudo !!`

If you just type `!!` and press enter, you'll be able to edit the command before executing it

If you just want to execute the last command, use the `r` alias

Press `esc .` to paste the last command's argument at the cursor's position

`$?` refers to the last command's error number

`^abc^def` display the last command, but replace abc with def

`?` any single character

`*` any amount of any characters

`[]` a class of characters, accepts a range as well

`<` redirect the file's contents as the input to a command

`>` redirect the output of a command into a file

## Background / foreground for terminal apps

`^z` to go back to the terminal

`fg` to go forward to the app

End a command with a ` & ` to make it run in the background

For example, you can use the youtube-dl program and make download the file in the background

## Command history search

`history` lists all the previous commands with numbers before them

`!\d` execute the command number that you got by using history

`HISTTIMEFORMAT="%Y-%m-%d %T "` That's how you enable the time for the history command

Doesn't work in zsh ^

`ctrl r` to pop into backward search

`ctrl s` to pop into forward search

Keep pressing it to go through the available search results

## Chaining commands

`;` works like a singlular try statement: will execute all commands even if any of them fail

`git add .; git commit -m "first commit"; git push` - all that in a single line, and it does its thing by itself, but regardless of whether any of them fail

This way you can easily set up a few commands that might take a while and not have to wait for all of them individually, just all of them together

`&&` is that, but won't execute the following commands if one fails

Use a ` & ` at the end of the command to run it in the background

## Paths and files

`filename{1..10}` will catch filename1, filename2, filename3, etc up to 10 (including)

`mkdir -p folder/folder/folder` lets you create multiple folders at a time

## Zsh keybindings

[gist](https://gist.github.com/2KAbhishek/9c6d607e160b0439a186d4fbd1bd81df)

`Alt + f / b` previous / next word

`Ctrl + a / e` start / end of the line

`Ctrl + shift + _` undo

`Ctrl + t` transpose two characters