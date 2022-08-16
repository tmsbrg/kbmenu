# kbmenu

Fork of dmenu, little hack that allows creating keyboard driven menus

Used in my `thomas-menu` script with the following content:

```sh
#!/bin/bash
run=$(<$HOME/Documents/keymenu.txt kbmenu -l 20 -b | cut -d' ' -f 2-)
bash <<< "$run"
```

keymenu.txt contains a key (or sequence of keys) followed by a space, followed by a command to execute. Example:
```
a your-awesome-script.sh
c sleep 0.1s && xdotool key ctrl+c
f wmctrl -a firefox
m sleep 0.1s && xdotool type "<your long email address>"
v sleep 0.1s && xdotool key ctrl+v
y mpv "https://www.youtube.com/watch?v=dQw4w9WgXcQ"
```

[My article on avoiding RSI that lead to creating the kbmenu hack](https://thomasvanderberg.nl/blog/kbmenu-dmenu-hack-keyboard-menu/)

[Original website for dmenu](https://tools.suckless.org/dmenu/)
