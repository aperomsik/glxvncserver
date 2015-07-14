# glxvncserver

glxvncserver is a wrapper script derived from the "vnc4server" script provided with the Ubuntu package of the same name. Instead of launching Xvnc, it launches Xorg with the dummy driver, and launches x11vnc to expose the Xorg session as a VNC session.

### Basic usage

```
glxvncserver :2
  launch the server as display :2, with x11vnc listening on port 5902

glxvncserver -kill :2
  kill the server launched via the command above
```

Other vnc4server parameters may also work.

### Requirements

* Xorg dummy_drv 
* x11vnc

For ubuntu, install them with "`sudo apt-get install x11vnc xserver-xorg-video-dummy`" .

### Acknowledgements

* Thanks to xpra.org, for [documenting](https://www.xpra.org/trac/wiki/Xdummy) that this could work, and providing a suitable [xorg.conf](http://xpra.org/xorg.conf) which I have included with minor adjustments.
