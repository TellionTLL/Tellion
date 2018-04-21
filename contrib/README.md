
Debian
====================
This directory contains files used to package telliond/tellion-qt
for Debian-based Linux systems. If you compile telliond/tellion-qt yourself, there are some useful files here.

## tellion: URI support ##


tellion-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install tellion-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your tellionqt binary to `/usr/bin`
and the `../../share/pixmaps/tellion128.png` to `/usr/share/pixmaps`

tellion-qt.protocol (KDE)

