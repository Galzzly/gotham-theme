# Gotham Theme

Gotham is a flat theme with transparent elements for GTK 3, GTK 2 and Gnome-Shell which supports GTK 3 and GTK 2 based desktop environments like Gnome, Unity, Budgie, Pantheon, XFCE, Mate, etc. This theme is a fork of the original Arc Theme Gotham project created by  0xhjohnson. Gotham is a very dark theme that is based off the Gotham Vim project by whatyouhide.

### Gotham is available in three variants

### Gotham

![A screenshot of the Gotham theme](http://i.imgur.com/AqEJ2oV.png)

### Gotham-Darker

![A screenshot of the Gotham-Darker theme](http://i.imgur.com/fjRAobi.png)

### Gotham-Dark (Recommended)

![A screenshot of the Gotham-Dark theme](http://i.imgur.com/qbfCnHo.png)


### Requirements

* Gnome/GTK3 3.14 - 3.22
* The `gnome-themes-standard` package
* The murrine engine. This has different names depending on your distro.
  * `gtk-engine-murrine` (Arch Linux)
  * `gtk2-engines-murrine` (Debian, Ubuntu, elementary OS)
  * `gtk-murrine-engine` (Fedora)
  * `gtk2-engine-murrine` (openSUSE)
  * `gtk-engines-murrine` (Gentoo)

Main distributions that meet these requirements are

* Arch Linux and Arch Linux based distros
* Ubuntu 15.04 or newer (**Ubuntu 14.04 and 14.10 are not supported**)
* elementary OS Freya/Loki
* Debian 8, Testing or Unstable
* Gentoo
* Fedora 21 or newer
* openSUSE 13.2, Leap 42.1 and Tumbleweed

Derivatives of these distributions should work, as well.

If your distribution isn't listed, please check the requirements yourself.

### Installation

**Important:** Remove all older versions of the theme from your system before you proceed any further.

    sudo rm -rf /usr/share/themes/{Gotham,Gotham-Darker,Gotham-Dark}
    rm -rf ~/.local/share/themes/{Gotham,Gotham-Darker,Gotham-Dark}
    rm -rf ~/.themes/{Gotham,Gotham-Darker,Gotham-Dark}

#### Manual Installation

To build the theme you'll need
* `autoconf`
* `automake`
* `pkg-config` or `pkgconfig` if you use Fedora
* `libgtk-3-dev` for Debian based distros or `gtk3-devel` for RPM based distros
* `git` if you want to clone the source directory

If your distribution doesn't ship separate development packages you just need GTK 3 instead of the `-dev` packages.

Install the theme with the following commands

**1. Get the source**

If you want to install the latest version from git, clone the repository with

    git clone https://github.com/Galzzly/gotham-theme.git --depth 1 && cd gotham-theme

**2. Build and install the theme**

    ./autogen.sh --prefix=/usr
    sudo make install

Other options to pass to autogen.sh are

    --disable-transparency     disable transparency in the GTK3 theme
    --disable-light            disable Gotham Light support
    --disable-darker           disable Gotham Darker support
    --disable-dark             disable Gotham Dark support
    --disable-cinnamon         disable Cinnamon support
    --disable-gnome-shell      disable GNOME Shell support
    --disable-gtk2             disable GTK2 support
    --disable-gtk3             disable GTK3 support
    --disable-metacity         disable Metacity support
    --disable-unity            disable Unity support
    --disable-xfwm             disable XFWM support

    --with-gnome=<version>     build the theme for a specific Gnome version (3.14, 3.16, 3.18, 3.20)
                               Note: Normally the correct version is detected automatically and this
                               option should not be needed.

After the installation is complete you can activate the theme with `gnome-tweak-tool` or a similar program by selecting `Gotham`, `Gotham-Darker` or `Gotham-Dark` as Window/GTK+ theme and `Gotham` or `Gotham-Dark` as Gnome-Shell and Xfce-Notify theme.

**Uninstall the theme**

Run

    sudo make uninstall

from the same directory as this README resides in, or

    sudo rm -rf /usr/share/themes/{Gotham,Gotham-Darker,Gotham-Dark}

### Extras

#### Chrome/Chromium theme (Gotham version in progress)
To install the Chrome/Chromium theme go to the `extra/Chrome` folder and drag and drop the gotham-theme.crx or gotham-dark-theme.crx file into the Chrome/Chromium window. The source of the Chrome themes is located in the source "Chrome/gotham-theme" folder.

#### Plank theme (Gotham version in progress)
To install the Plank theme, copy the `extra/Gotham-Plank` folder to `~/.local/share/plank/themes` or to `/usr/share/plank/themes` for system-wide use.
Now open the Plank preferences window by executing `plank --preferences` from a terminal and select `Gotham-Plank` as the theme.

### Troubleshooting

If you have Ubuntu with a newer GTK/Gnome version than the one included by default (i.e Ubuntu 14.04 with GTK 3.14 or Ubuntu 15.04 with GTK 3.16, etc.) the prebuilt packages won't work properly and you have to install the theme manually as described above.
This is also true for other distros with a different GTK/Gnome version than the one included by default

--

If you get artifacts like black or invisible backgrounds under Unity, disable overlay scrollbars with

    gsettings set com.canonical.desktop.interface scrollbar-mode normal


### Bugs
If you find a bug, please report it at https://github.com/Galzzly/gotham-theme/issues

### License
Gotham is available under the terms the GPL-3.0. See `COPYING` for details.

### Full Preview
![A full screenshot of the Gotham theme](http://i.imgur.com/bNaPB1b.png)
<sub>Screenshot Details: Icons: [Numix Circle](https://github.com/numixproject/numix-icon-theme-circle) | Font: Fira Sans</sub>


[sk-overlay]: https://c.darenet.org/scriptkitties/overlay
