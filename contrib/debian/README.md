
Debian
====================
This directory contains files used to package cryptond/crypton-qt
for Debian-based Linux systems. If you compile cryptond/crypton-qt yourself, there are some useful files here.

## crypton: URI support ##


crypton-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install crypton-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your crypton-qt binary to `/usr/bin`
and the `../../share/pixmaps/bitcoin128.png` to `/usr/share/pixmaps`

crypton-qt.protocol (KDE)

