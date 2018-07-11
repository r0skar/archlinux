# archlinux

Archlinux desktop settings and things to remember.

## HIDPI

- Fractional scaling introduces a lot of problems. Avoid it!
- Optimal setup: Scale display to x2. Force font DPI to 154.
  - Firefox scaling: set `layout.css.devPixelsPerPx` to 1.7 in `about:config`
  - `export PLASMA_USE_QT_SCALING=1` in `.bash_profile` to enable scaling of plasma panels and desktop

## Global Menu

- Install `appmenu-gtk-module`, `libdbusmenu-glib`, `libdbusmenu-gtk3`, `libdbusmenu-gtk2`
- Go to Settings / Application style / Window Decorations / Buttons and add the global menu button.
  - Alternative is to use a global menu panel.

## Firefox

- Use `firefox-kde-opensuse-bin`
  - includes global menu
  - includes KDE file dialogs

## Node JS

- Global yarn packages are installed into `/home/oskar/.config/yarn/global/`, while the global executables are in `/home/oskar/.yarn/bin/`.

## Theming

- Breeze AlphaBlack: Disable the theming of windows:
  - Comment out Line 200 `setTitlebarColors(newColor)` in `/home/oskar/.local/share/plasma/desktoptheme/breeze-alphablack/desktoptheme.py`
- Folder Icons: Replaced the default Breeze theme folders (`places`) with [Nix OS folders](https://www.opendesktop.org/p/1228310/)

## Dolphin

- Service Menus
  - Service menus are defined in `/home/oskar/.local/share/kservices5/`

## AUR

- Use [yay](https://github.com/Jguer/yay) instead of pacaur.

## KWIN

- Use patched KWIN to enable middle-click close and disable hover effects in Present Window Effect:
  - The custom PKGBUILD contains the key `groups=('patched')`, which makes sure that pacman ignores official updates for the modified packages.
  - Edit `PKGBUILD`, `middleclick-close-window.patch` and `no-hover-scale.patch` and update KWIN versions.
  - Generate KWIN using `makepkg --skippgpcheck`.
  - Install patched KWIN with `sudo pacman -U kwin-VERSION.tar.xz`
