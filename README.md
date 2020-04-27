# Midnight Ubuntu Theme
## Files:
* `gdm-theme` - Contains the theming of gnome-shell which also applies to GDM (Gnome Display Manager). 
* `gnome-shell`, `gtk-2.0` and `gtk-3.0` - Contains theming of window and gnome shell for desktop.
* `conky` - Widget application that can be run as a background process.

## Installation:
### `gdm-theme`
1.) You may want to make a backup copy of your ubuntu.css in the theme folder.
```bash
cd /usr/share/gnome-shell/theme
sudo cp ubuntu.css ubuntu.css.bak
```

2.) Copy the contents in folder `gdm-theme` that you downloaded to the theme folder.
```bash
sudo cp * /usr/share/gnome-shell/theme
```
To revert GDM theme back, you can simply copy the original content back to your `ubuntu.css` folder:
```bash
cd /usr/share/gnome-shell/theme
sudo cp ubuntu.css.bak ubuntu.css
```

DISCLAIMER:
* Color scheme was copied from midnight theme.
* I made changes to the ubuntu.css file to annotate my gdm theme.
* Inspired by the themes that were used here.
* Most of the images are obtained from [this repository](https://github.com/i-mint/midnight).

### `gnome-themes`
Requisites: GNOME tweaks.

1.) Copy/move the following folders (`gnome-shell`, `gtk-2.0` and `gtk-3.0`) to your theme folder.
```bash
# If you want to make the theme available to yourself only.
mkdir ~/.themes
cp -R gnome-shell gtk-2.0 gtk-3.0 ~/.themes

# Or to every user with the account of your computer (requires at least sudo permissions).
mkdir /usr/share/themes/midnight-green
sudo cp -R gnome-shell gtk-2.0 gtk-3.0 /usr/share/themes/midnight-green
```

DISCLAIMER:
* The contents of `gtk-2.0`, `gtk-3.0` and `gnome-shell` are actually archive copies of the midnight theme and were obtained from [this repository](https://github.com/i-mint/midnight).

### `conky`
Requisites: conky (Install using apt)

OPTIONAL: You can copy the contents of the `conky` folder to a hidden folder `i.e mkdir ~/.startup && cd ~/.startup`.

Create a startup bash file with the content in your conky folder:
```bash
#!/bin/bash

sleep 10
conky -b -q -c act.conkyrc &
conky -b -q -c sys.conkyrc &
conky -b -q -c clk.conkyrc & 
exit
```
Also keep in mind you can delete any of the 3 lines if you do not want to load one of them.