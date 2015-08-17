# $Id: PKGBUILD 46079 2011-05-03 10:20:22Z spupykin $
# Maintainer: Sergej Pupykin <pupykin.s+arch@gmail.com>
# Contributor: ansgras <ataflinski@uni-koblenz.de>

pkgname=synce-hal
pkgver=0.15
pkgrel=1
pkgdesc="hal based alternative for SynCE dccm"
arch=('i686' 'x86_64')
url="http://synce.sourceforge.net/"
license=('GPL')
depends=('synce-libsynce' 'gnet' 'dhclient' 'hal' 'dbus')
source=(http://switch.dl.sf.net/sourceforge/synce/synce-hal-$pkgver.tar.gz)
md5sums=('796eca27a2ce561247e7a71375c242b6')

build() {
  cd $srcdir/$pkgname-$pkgver
  ./configure --prefix=/usr --libexecdir=/usr/lib/$pkgname \
	 --with-hal-addon-dir=/usr/lib/hal/scripts
  make
}

package() {
  cd $srcdir/$pkgname-$pkgver
  make DESTDIR="$pkgdir/" install
}
