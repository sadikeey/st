st - simple terminal
--------------------
st is a simple terminal emulator for X which sucks less.


Requirements
------------
In order to build st you need the Xlib header files.

- On Debian/Ubuntu
```sh
sudo apt install build-essential libx11-dev libxft-dev libxinerama-dev libfreetype6-dev libfontconfig1-dev
```

- On Arch Linux

```sh
sudo pacman -S base-devel libx11 libxft libxinerama freetype2 fontconfig
```

- On Fedora/RHEL

```sh
sudo dnf install make cmake gcc libX11-devel libXft-devel libXinerama-devel libXrandr-devel
```

- On Void Linux(case sensitive)

```sh
sudo xbps-install base-devel libX11-devel libXft-devel libXinerama-devel freetype-devel fontconfig-devel
```

Installation
------------
Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

    make clean install


Running st
----------
If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.

Credits
-------
Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.

