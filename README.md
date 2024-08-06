# disable-secondmonitor-sddm-login
The following command and script disables second monitor on login screen on sddm kde arch linux

on console type to list connected monitors
``` xrandr | grep -w connected ```
This wil give you the list of connected monitors:

DVI-I-1
HDMI-1

After identifying your second monitor 
Type `sudo nano /usr/share/sddm/scripts/Xsetup `
paste 
 - ```xrandr --output HDMI-1 --off``` 
`
#!/bin/sh
Xsetup - run as root before the login dialog appears
xrandr --output HDMI-1 --off
`
Then finally reboot.

