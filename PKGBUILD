# Maintainer : Martin Wimpress <code@flexion.org>
# Contributor: Giovanni "Talorno" Ricciardi <kar98k.sniper@gmail.com>
# Contributor: Xpander <xpander0@gmail.com>

pkgname=mate-dialogs
pkgver=1.6.2
pkgrel=3
pkgdesc="Display graphical dialog boxes from shell scripts"
url="http://mate-desktop.org"
arch=('i686' 'x86_64' 'armv6h' 'armv7h')
license=('LGPL')
depends=('gtk2' 'libnotify')
makedepends=('docbook-xml' 'mate-common' 'mate-doc-utils' 'perl-xml-parser')
options=('!emptydirs')
groups=('mate')
source=("http://pub.mate-desktop.org/releases/1.6/${pkgname}-${pkgver}.tar.xz")
sha1sums=('64601ae71671911dbc83d1fab2a837da0b218cf9')

build() {
    cd "${srcdir}/${pkgname}-${pkgver}"
    ./configure \
        --prefix=/usr \
        --disable-scrollkeeper
    make
}

package() {
    cd "${srcdir}/${pkgname}-${pkgver}"
    make DESTDIR="${pkgdir}" install
}
