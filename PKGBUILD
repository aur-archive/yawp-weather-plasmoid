# Maintainer: Carl Mueller arch at carlm e4ward com

pkgname=yawp-weather-plasmoid
pkgver=0.4.3
pkgrel=1
pkgdesc="Colorful kdeplasma weather widget"
arch=(i686 x86_64)
url="http://www.kde-look.org/content/show.php/yaWP+(Yet+Another+Weather+Plasmoid)?content=94106"
depends=('kdebase-workspace' 'gettext')
makedepends=('cmake' 'automoc4')
conflicts=(kde-extragear-plasmoids)
source=(http://downloads.sourceforge.net/yawp/yawp-$pkgver.tar.bz2)
license=('GPL')
md5sums=('02af5ff62c5b05a9db034bae6c5f72c2')
build() {
  cd $srcdir/yawp-$pkgver
  mkdir build
  cd build
  cmake -DCMAKE_INSTALL_PREFIX=`kde4-config --prefix` ..
  make VERBOSE=1
  make DESTDIR=$pkgdir install
}
