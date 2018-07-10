# archlinux
Archlinux desktop settings and things to remember.

## HIDPI
- Fractional scaling introduces a lot of problems. Avoid it!
- Optimal setup: Scale display to x2. Force font DPI to 154.
  - Firefox scaling: set 'layout.css.devPixelsPerPx' to 1.7
  
## Global Menu
- Install `appmenu-gtk-module`, `libdbusmenu-glib`, `libdbusmenu-gtk3`, `libdbusmenu-gtk2`
- Go to Settings / Application style / Window Decorations / Buttons and add the global menu button.
  - Alternative is to use a global menu panel.

## Firefox
- Use `firefox-kde-opensuse-bin`
  - includes global menu
  - includes KDE file dialogs
