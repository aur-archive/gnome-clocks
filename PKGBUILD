# Maintainer: Yangtse Su <yangtsesu@gmail.com>

pkgname=gnome-clocks
pkgver=0.1.4
pkgrel=2
pkgdesc="Clock application designed for GNOME 3 "
arch=(any)
url="https://live.gnome.org/GnomeClocks"
license=('GPL')
groups=(gnome-extra)
depends=('python2-gobject>=3.4.0' 'gobject-introspection>=1.34.0' 'clutter-gtk>=1.3.2' 'libgweather' 'libnotify')
makedepends=('python2-distutils-extra')
install=gnome-clocks.install
source=(http://download.gnome.org/sources/$pkgname/${pkgver%.*}/$pkgname-$pkgver.tar.xz)
sha256sums=('0cb0ee16b268d1600dc40cb24ade1335a06d106401bc0dcc4a2f4fb8dee30cf9')

build() {
  cd $pkgname-$pkgver
  python2 ./setup.py build
}
package() {
  cd $pkgname-$pkgver
  python2 ./setup.py install --root="$pkgdir" -O1
}
# vim:set ts=2 sw=2 et:
