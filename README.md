# spaceI3

Spacemacs inspired i3wm configuration implemented by using the modal key binding feature of i3.

Ideally all the i3 commands can be achieved by using some mode.

http://spacemacs.org/

# Work in progress...
For the time being is tested on a laptop with ubuntu.

For the time being this configuration mixes 3 aspects
 * The I3 configuration for modal key-bidings.
 * The Visuals configuration such as fonts colors and borders.
 * Some desktop environment configuration, such as wallpapers, applets, etc.

This coupling might change in the future.


# Default I3 configuration override
When I3 default configuration does not work shall be documented in this section.

 * *jkl;* replaced by *hjkl*, all the moving commands where replaced to match the VIM style.
  

| Key-binding | original          | SpaceI3         |
|-------------|-------------------|-----------------|
| $mod+space  | focus mode toggle | mode space mode |
| $mod+h      | layout horizontal | move focus left |


# Features

# Getting Started
Just Hit **$mod+space** and select what you want

**Escape** or **Return** returns to default mode.

**$mod+h|j|k|l** Move focus between windows

**$mod+Shift+h|j|k|l** Move windows

**$mod+f** Make window fullscreen

# De-uglify GTK and Qt apps/Theme configuration
Answer that works great from

    https://askubuntu.com/questions/598943/how-to-de-uglify-i3-wm

    sudo apt-get install lxappearance gtk-chtheme qt4-qtconfig

Start with lxappearance and choose a theme; then choose it in gtk-chtheme. In
qt4-config, there is a dropdown menu setting to make qt take the GTK+ settings.
That seems to work best for me. (It makes VLC and KeepassX look good.)

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

### Keyring daemon
Solution from https://wiki.archlinux.org/index.php/GNOME/Keyring#Using_the_keyring_outside_GNOME

in /etc/zsh/zshenv add
```
if [ -n "$DESKTOP_SESSION" ];then
    eval $(gnome-keyring-daemon --start)
    export SSH_AUTH_SOCK
fi
```
This will sart the daemon when login to i3 from lighdm.

## Applications Launcher
 * sensible-browser
 * i3-sensible-terminal
 * nautilus
 * rofi
