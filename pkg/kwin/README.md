# kwin

- Edit `PKGBUILD` and all `*.patch` files to include the new KWIN version.
- Generate KWIN using `makepkg --skippgpcheck`.
- Install patched KWIN with `sudo pacman -U kwin-VERSION.tar.xz`

Note: Use `makepkg -o --skippgpcheck` to download and extract original package.
