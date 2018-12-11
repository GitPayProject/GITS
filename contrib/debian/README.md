
Debian
====================
This directory contains files used to package GITSd/GITS-qt
for Debian-based Linux systems. If you compile GITSd/GITS-qt yourself, there are some useful files here.

## GITS: URI support ##


GITS-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install GITS-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your GITSqt binary to `/usr/bin`
and the `../../share/pixmaps/GITS128.png` to `/usr/share/pixmaps`

GITS-qt.protocol (KDE)

