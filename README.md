g3kb-switch
===========

This is a keyboard layout switcher for Gnome 3. It is not based on the X
interface but rather implements direct D-Bus messaging with the Gnome Shell.

Installation
------------

Build as a normal user.

```ShellSession
    $ mkdir build && cd build
    $ cmake ..
    $ make
```

Install being a superuser.

```ShellSession
    # make install
```

Usage
-----

```ShellSession
Usage: g3kb-switch -s ARG    Sets current layout group to ARG
       g3kb-switch -l        Displays all layout groups
       g3kb-switch -h        Displays this message
       g3kb-switch -v        Shows version number
       g3kb-switch [-p]      Displays current layout group
```

Integration with vim-xkbswitch
------------------------------

Basically, put in *.vimrc* lines

```vim
let g:XkbSwitchEnabled = 1
let g:XkbSwitchLib = '/usr/local/lib/libg3kbswitch.so'
```

See details about configuration rules for vim-xkbswitch
[here](https://github.com/lyokha/vim-xkbswitch#basic-configuration).
