# Maintainer: John Jenkins <twodopeshaggy@gmail.com>
# Contributor: Maxime Gauduin <alucryd@gmail.com>
# Contributor: Balló György <ballogyor+arch@gmail.com>

pkgname=libunity
pkgver=7.1.4
pkgrel=6
pkgdesc='Library for instrumenting and integrating with all aspects of the Unity shell'
arch=('i686' 'x86_64')
url='https://launchpad.net/libunity'
license=('LGPL')
depends=('dee' 'gtk3' 'libdbusmenu-glib')
makedepends=('gnome-common' 'gobject-introspection' 'intltool' 'vala')
source=("https://launchpad.net/ubuntu/+archive/primary/+files/libunity_$pkgver+17.10.20170605.orig.tar.gz")
sha256sums=('SKIP')

build() {
  cd ${srcdir}
  ./autogen.sh --prefix='/usr' --sysconfdir='/etc' --localstatedir='/var' --disable-static
  make
}

package() {
  cd ${srcdir}
  make DESTDIR="${pkgdir}" install
}
