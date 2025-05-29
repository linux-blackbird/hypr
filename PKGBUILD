# Maintainer: Al Muhdil Karim <caleb@alerque.com>

pkgname=hyprdev
pkgver=0.0.1
pkgrel=1
arch=(x86_64)
url='https://github.com/linux-blackbird/hyprdev'
pkgdesc="blackbird hyprland config"
license=('MIT-License')
groups=()
depends=(hyprland
         hyprlock
         hypridle)
makedepends=()
optdepends=()
source=()
#sha256sums=(SKIP)

package(){

    if [ ! -d $pkgdir/usr/share/hypr ];then
        mkdir -p $pkgdir/usr/share/hypr
    fi

    if [ ! -d $pkgdir/etc/skel/.config/hypr/ ];then
        mkdir -p $pkgdir/etc/skel/.config/hypr/
    fi

    if [ -f $pkgdir/usr/share/hypr/wall0.png ];then
        rm $pkgdir/usr/share/hypr/wall0.png
    fi

    if [ -f $pkgdir/usr/share/hypr/wall1.png ];then
        rm $pkgdir/usr/share/hypr/wall1.png
    fi

    if [ -f $pkgdir/usr/share/hypr/wall2.png ];then
        rm $pkgdir/usr/share/hypr/wall2.png
    fi

    if [ -f $pkgdir/etc/skel/.config/hypr/hyprland.conf ];then
        rm $pkgdir/etc/skel/.config/hypr/hyprland.conf
    fi

    install -D -m644 $srcdir/etc/hyprland.conf $pkgdir/etc/skel/.config/hypr/
    install -D -m755 $srcdir/img/* $pkgdir/usr/share/hypr/
}