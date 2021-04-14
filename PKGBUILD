# $Id$
# Maintainer: James Kittsmiller (AJSlye) <james@nulogicsystems.com>

pkgname=deepin-diskmanager
pkgver=1.2.8
pkgrel=1
pkgdesc="Disk management tool for creating, reorganizing and formatting partitions."
arch=("x86_64")
url="https://www.deepin.com/"
license=("GPL3")
groups=('deepin-manjaro')
depends=('deepin-qt-dbus-factory' 'dtkwidget' 'parted' 'polkit-qt5' 'smartmontools')
source=("https://community-packages.deepin.com/deepin/pool/non-free/d/deepin-diskmanager/deepin-diskmanager_${pkgver}-1_amd64.deb")
sha512sums=('984dad6896edf3ccd534b0a54f6e3e69d5d47d08ad0f08eb12b21189540281a20942d5f38f3df8b0fa72a3773180c00c7cf706d61129d069982b8908d535df1c')

package(){
    cd ${srcdir}
    tar -xJvf data.tar.xz -C "${pkgdir}"
    cd ${pkgdir}
    sed -i "s|GenericName=diskmanager|GenericName=Diskmanager|" usr/share/applications/deepin-diskmanager.desktop
    cp -R lib usr
    rm -R lib
}
