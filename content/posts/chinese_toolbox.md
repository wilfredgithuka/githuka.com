---
title: "中文版的电脑软件 Linux Chinese Software"
date: 2020-10-13T10:39:04+03:00
draft: false
---
The following is a list of applictions that I use in a Chinese
environment which I think might be useful to my readers.

## Document Processing

### WPS Office Linux
```
yay -S wps-office
```
### PDF

* [MuPDF](https://mupdf.com/) is Very fast EPUB, FictionBook, PDF, XPS and Comicbook viewer written in portable C. Features CJK font support.
* [Okular](https://https://okular.kde.org/) — Universal document viewer for KDE. Supports CHM, Comicbook, DjVu, DVI, EPUB, FictionBook, Mobipocket, ODT, PDF, Plucker, PostScript, TIFF and XPS.
* [Zathura](https://pwmt.org/projects/zathura) — Highly customizable and functional document viewer (plugin based). Supports PDF, DjVu, PostScript and Comicbook.

```
sudo pacman -S okular mudpf zathura mupdf-tools
```
This [page](https://wiki.archlinux.org/index.php/PDF) gives alot of info about manulilation of PDFs, which is a good read.

## Graphics

### Screenshot

* Xfce4 Screenshooter — Application and Xfce4 panel plugin to take screenshots about the entire screen, 
the active window or a selected region. Part of xfce4-goodies. [xfce4-screenshoter](http://goodies.xfce.org/projects/applications/xfce4-screenshooter)

```
sudo pacman -S xfce4-screenshooter
```
