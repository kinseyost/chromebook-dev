# Developing on Chromebook
Chromebook has some quirks when developing, I'm hoping to flesh some of those out.

I am using [crouton](https://github.com/dnschneid/crouton) which has proven to be *amazing*.  One issue I have run into however is running services/daemons/servers on the chroot that crouton provides.

### Installing mongodb
If you've never installed mongodb, you may have some issues with permissions and file directories which you will need to resolve. Simply create the missing directories, and `chmod` The appropriate folder.

### Running servers
Recently I found this link in the wiki:
* [running servers in crouton](https://github.com/dnschneid/crouton/wiki/Running-servers-in-crouton)

### Changing keys in crouton to work like chromebook
* [keyboard](https://github.com/dnschneid/crouton/wiki/Keyboard)

### Natural Scrolling
If you have tried via the ui to enable natural scrolling, and that doesn't work, check [this](http://askubuntu.com/a/278849) out.
Open synaptics settings with your favorite editor with sudo priveleges.
```
sudoedit /usr/share/X11/xorg.conf.d/50-synaptics.conf
```
Navigate to the section "InputClass" Identifier "touchpad catchall"
```
Option "VertScrollDelta" "-55"
Option "HorizScrollDelta" "-55"
```

Save and reboot.

If you wanna play around with the speed of scroll change -55 to whatever works best for you.  You can get an idea by changing the `ScrollDeltas` for each of these using synclient. (doesn't require reboot).
```
synclient VertScrollDelta=-55
synclient HorizScrollDelta=-55
```



  - Though, -111 is a little slow for me, I changed it to -51 for both `VertScrollDelta`, and `HorizScrollDelta`
