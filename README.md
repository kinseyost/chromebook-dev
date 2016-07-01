# Developing on Chromebook
Chromebook has some quirks when developing, I'm hoping to flesh some of those out.

I am using [crouton](https://github.com/dnschneid/crouton) which has proven to be *amazing*.  One issue I have run into however is running services/daemons/servers on the chroot that crouton provides.

### Running servers
Recently I found this link in the wiki:
* [running servers in crouton](https://github.com/dnschneid/crouton/wiki/Running-servers-in-crouton)

### Changing keys in crouton to work like chromebook
* [keyboard](https://github.com/dnschneid/crouton/wiki/Keyboard)

### Natural Scrolling
If you have tried via the ui to enable natural scrolling, and that doesn't work, check [this](http://askubuntu.com/a/278849) out.
  - Though, -111 is a little slow for me, I changed it to -51 for both `VertScrollDelta`, and `HorizScrollDelta`
