# DWM - dynamic window manager
dwm is an extremely fast, small, and dynamic window manager for X.


Dependencies
- In order to build dwm you need the Xlib header files.
- maim
- dmenu


## Installation
```bash
make clean install
```


## Running dwm
Add the following line to your .xinitrc to start dwm using startx:

```bash
exec dwm
```

In order to connect dwm to a specific display, make sure that
the DISPLAY environment variable is set correctly, e.g.:

```bash
DISPLAY=foo.bar:1 exec dwm
```

(This will start dwm on display :1 of the host foo.bar.)

In order to display status info in the bar, you can do something
like this in your .xinitrc:

```bash
while xsetroot -name "`date` `uptime | sed 's/.*,//'`"
do
    sleep 1
done &
exec dwm
```
