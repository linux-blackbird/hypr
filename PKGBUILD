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

    if [ -e $pkgdir/usr/share/hypr/wall0.png ];then
        sudo rm $pkgdir/usr/share/hypr/wall0.png
    fi

    if [ -e $pkgdir/usr/share/hypr/wall1.png ];then
        sudo rm $pkgdir/usr/share/hypr/wall1.png
    fi

    if [ -e $pkgdir/usr/share/hypr/wall2.png ];then
        sudo rm $pkgdir/usr/share/hypr/wall2.png
    fi

    if [ -e $pkgdir/etc/skel/.config/hypr/hyprland.conf ];then
        sudo rm $pkgdir/etc/skel/.config/hypr/hyprland.conf
    fi

    sudo cp -f $srcdir/etc/hyprland.conf $pkgdir/etc/skel/.config/hypr/
    sudo cp -f $srcdir/img/* $pkgdir/usr/share/hypr/
}