# $Id$
# Maintainer: James Kittsmiller (AJSlye) <james@nulogicsystems.com>

pkgname=deepin-diskmanager
pkgver=1.1.0.34
pkgrel=1
pkgdesc="Disk management tool for creating, reorganizing and formatting partitions."
arch=("x86_64")
url="https://www.deepin.com/"
license=("GPL3")
groups=('deepin-manjaro')
depends=('deepin-qt-dbus-factory' 'dtkwidget' 'parted' 'polkit-qt5' 'smartmontools')
source=("https://community-packages.deepin.com/deepin/pool/non-free/d/deepin-diskmanager/deepin-diskmanager_${pkgver}-1_amd64.deb")
sha512sums=('56bc10d9f93a626f87220fe6d13f25706f609a64836968187e1236f0db76b6add05ad4caba2da0b874704aeb8306b7f39aff1115697589aa5482e327de3c784e')

package(){
    cd ${srcdir}
    tar -xJvf data.tar.xz -C "${pkgdir}"
    cd ${pkgdir}
    sed -i "s|GenericName=diskmanager|GenericName=Diskmanager|" usr/share/applications/deepin-diskmanager.desktop
    cp -R lib usr
    rm -R lib
}
