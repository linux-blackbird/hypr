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

    if [ ! -d /usr/share/hypr ];then
        mkdir -p /usr/share/hypr
    fi

    if [ ! -d /etc/skel/.config/hypr/ ];then
        mkdir -p /etc/skel/.config/hypr/
    fi

    install -D -m644 $pgkdir/etc/hyprland.conf /etc/skel/.config/hypr/
    install -D -m755 $pgkdir/img/* /usr/share/hypr/
}