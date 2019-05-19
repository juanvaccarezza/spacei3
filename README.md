# spacei3
Spacemacs inspired i3wm configuration 

http://spacemacs.org/

Work in progress...

For the time being is tested on a laptop with ubuntu.

# Features

# Getting Started
Just Hit **$mod+space** and select what you want

**Escape** or **Return** returns to default mode.

**$mod+h|j|k|l** Move focus between windows

**$mod+Shift+h|j|k|l** Move windows

**$mod+f** Make window fullscreen

**$mod+d** Run rofi

# De-uglify GTK and Qt apps/Theme configuration
Answer that works great from 

    https://askubuntu.com/questions/598943/how-to-de-uglify-i3-wm

    sudo apt-get install lxappearance gtk-chtheme qt4-qtconfig

Start with lxappearance and choose a theme; then choose it in gtk-chtheme. In qt4-config, there is a dropdown menu setting to make qt take the GTK+ settings. That seems to work best for me. (It makes VLC and KeepassX look good.)

# Dependencies & Programs
## Desktop integration
 * xrandr (Outputs management)
 * nm-applet (Network manager applet)
 * blueman-applet (Bluetooth applet)
 * xfce4-power-manager (Brightness control keys and Battery status)
 * xautolock (Automatic screen locking)
 * systemctl (System interface for hibernate, suspend, reboot)
 * nitrogen (Wallpaper)
 * lightdm (dm-tool lock)

## Applications Launcher
 * sensible-browser
 * i3-sensible-terminal
 * nautilus
 * rofi

