# Contributor: Allen Li <darkfeline (at) abagofapples.com>

pkgname=projectm-jack
pkgver=2.1.0
pkgrel=3
pkgdesc="projectM frontend for visualizing the output of the JACK Audio Connection Kit."
url="http://projectm.sourceforge.net"
arch=('i686' 'x86_64')
license=('GPL')
groups=('projectm-jack')
depends=('projectm' 'projectm-qt' 'jack')
makedepends=('pkgconfig' 'xproto' 'cmake')
source=(http://sourceforge.net/projects/projectm/files/$pkgver/projectM-complete-$pkgver-Source.tar.gz)
md5sums=(debf30f7ce94ff0102f06fbb0cc4e92b)

build() {
  cd $srcdir/projectM-complete-$pkgver-Source/src/projectM-jack
  cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr .
  make
  make DESTDIR=$pkgdir install
}

