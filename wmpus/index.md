Getting started
---------------
* The [manual](manual) has usage information
* On win32, wmpus works best with Putty 0.61

Current features
----------------
Native support for X11 and MS Windows

Simple code base (small number of files, no automake, etc)

* Clean separation from the underlying windowing system
* Very few external dependencies (libc, libx11 and xinerama for sys-x11)

Tiling window management similar to [wmii]

* Support for multiple monitors
* Support for multiple desktops (i.e. tags)
* No toolbars/statusbars, use [dzen] instead

[wmii]: http://wmii.suckless.org/
[dzen]: http://sites.google.com/site/gotmor/dzen

Download
--------
Development code via git and [gitweb](/git/?p=wmpus)

    git clone git://pileus.org/wmpus

Windows binaries (snapshots):

* <http://pileus.org/wmpus/files/>

Development
-----------
To build wmpus for X11:

    make SYS=x11    # or simply make

To build wmpus for win32:

    make SYS=win32

The following features will likely be added at some point:

* Window decorations/titlebars for sys-x11
* Configurable key bindings
* All the features listed in the Issues tracker
