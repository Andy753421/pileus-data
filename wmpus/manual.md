<div style="white-space:pre; font-family:monospace;">
WMPUS(1)                                                              WMPUS(1)

NAME
       wmpus - cross platform window manager

SYNOPSIS
       wmpus [OPTION..]

DESCRIPTION
       wmpus  is portable window manager. Currently it supports wmii like win‐
       dow management and includes x11 and win32 backends.

OPTIONS
       -n, --no-capture
              Do not arrange pre-existing windows

       -b, --border=N
              Draw an n pixel window border

       -m, --margin=N
              Leave an n pixel margin around windows

       -i, --int=KEY=NUM
              Set integer configuration option

       -s, --str=KEY=STR
              Set string configuration option

       -h, --help
              Print usage information

CONFIGURATION
       Wmpus supports a simple ini-like configuration file stored in the users
       home directory. Currently supported configuration options include:

   Main section
       no-capture=[01]
              Do not arrange pre-existing windows. Same as -n

       border=N
              Border width in pixels to draw around windows. X11 only, default
              2. Same as -b

       margin=N
              Margin in pixels between windows for  wm-wmii.  X11  default  0,
              Win32 default 15.  Same as -m

       stack=N
              Height  in pixels for non-focused windows when the column is set
              to stack layout

COMPILE-TIME OPTIONS
       The windowing system backend and window management modes can be changed
       at  compile-time  by linking in the correct object file. Supported win‐
       dowing systems include X11 (sys-x11.c) and Windows (sys-win32.c).  Sup‐
       ported window management modes include WMII like window management (wm-
       wmii.c) and a simple tags based virtual-desktop manager (wm-tags.c).

       In addition several pre-processor settings are available which  can  be
       set in config.mk or on the command line:

       MODKEY=key
              Modifier used for window management commands, can be either alt,
              ctrl, shift, or win. Default alt

       DEBUG  Enable various debugging functions

WMII WINDOW MANAGEMENT
       The wmii window management mode mimics the behavior of the wmii(1) win‐
       dow  manager.  By default, the alt- prefix is used for most window man‐
       agement commands and is used along with the h, j,  k,  and  l  keys  to
       focused different windows.

       The  alt-shift-  prefix is used for moving windows and works similar to
       changing the focus. The mouse is used for resizing windows and also for
       changing focus.

   Changing focus
       Alt-j  Focus window below the currently focused window

       Alt-k  Focus window above the currently focused window

       Alt-h  Focus column to the left of the currently focused column

       Alt-l  Focus column to the right of the currently focused column

   Moving windows around
       Alt-Shift-j
              Move the currently focused window down

       Alt-Shift-k
              Move the currently focused window up

       Alt-Shift-h
              Move the currently focused window to the left

       Alt-Shift-l
              Move the currently focused window to the right

   Column layouts
       Alt-d  Switch the current column to split layout

       Alt-s  Switch the current to stack layout

       Alt-m  Switch the current to maximized layout

   Tagging windows
       Alt-[0..n]
              Switch to tag n

       Alt-Shift-[0..n]
              Move the currently focused window to tag n

   Floating windows
       Alt-Space
              Toggle focus between the tiling and floating layers

       Alt-Shift-Space
              Move  the currently focused window between the tiling and float‐
              ing layers

   Other commands
       Alt-f  Toggle fullscreen for the focused window

       Alt-Shift-c
              Close the currently focused window

       Alt-Shift-q
              Restore all hidden windows and quit wmpus

       Alt-F5 Refresh the window layout (useful for debugging)

       Alt-F6 Dump a ASCII representation the window layout to standard output
              (useful for debugging)

   Mouse commands
       Pointer
              Moving the mouse over a window focuses that window

       Button1
              Click in a floating window brings it to the top

       Alt-Button1
              Click and drag moves a floating window under the cursor

       Alt-Button3
              Click and drag resizes the window under the cursor

X11 BACKEND
       The X11 backend draws a small 2px border around each window. The border
       for the currently focused window is set to a  lighter  color  than  the
       rest.

WIN32 BACKEND
       The  Win32  backend uses the existing window borders and title bars. It
       also leaves a narrow space between the windows so that they  look  more
       natural in a Windows environment.

FILES
       ~/.wmpus
              The wmpus configuration file

SEE ALSO
       wmii(1), dwm(1), dzen(1)

BUGS
       Many
</div>
