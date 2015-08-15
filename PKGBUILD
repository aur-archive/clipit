# maintainer: Mihai Militaru <mihai dot militaru at xmpp dot ro>

pkgname=clipit
pkgver=1.4.2
pkgrel=2
pkgdesc="Lightweight GTK+ clipboard manager (fork of Parcellite)"
arch=('i686' 'x86_64')
url="http://gtkclipit.sourceforge.net/"
license=('GPL3')
depends=('gtk2' 'hicolor-icon-theme')
makedepends=('intltool')
optdepends=('xdotool: for automatic paste')
source=(https://github.com/downloads/shantzu/ClipIt/${pkgname}-${pkgver}.tar.gz)
sha1sums=('e01d02a60efdac575f8c0f84ceef210be1466d1a')
install=clipit.install

build() {
  cd ${srcdir}/${pkgname}-${pkgver}
  ./configure --prefix=/usr --sysconfdir=/etc || return 1
  make || return 1
  make DESTDIR=${pkgdir} install || return 1
  gtk-update-icon-cache
}