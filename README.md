# Midnight Ubuntu Theme
## Files:
* gdm-theme - Contains the theming of my GDM (Gnome Display Manager). 

## Installation:
### GDM-THEME
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

## Disclaimer
GDM THEMES:
* I made changes to the ubuntu.css file to annotate my theme.
* Most of the images are obtained from [this repository](https://github.com/i-mint/midnight).
