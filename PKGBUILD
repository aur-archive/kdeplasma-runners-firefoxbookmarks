# Contributor: Tilo Brueckner  blueperil at gmx de

pkgname=kdeplasma-runners-firefoxbookmarks
pkgver=0.2.4
pkgrel=1
pkgdesc='A runner that integrates mozilla firefox bookmarks into krunner'
arch=('i686' 'x86_64')
url=(http://kde-apps.org/content/show.php/Browse+Firefox+Bookmarks?content=141042)
license=('GPL')
depends=('kdebase-workspace' 'firefox')
makedepends=('automoc4' 'cmake')
source=('http://kde-apps.org/CONTENT/content-files/141042-browsefirefoxbookmarks.tar.gz')
md5sums=('f1f49309ae712e5044cf7bd8384be0d9')
conflicts=('krunner-firefoxbookmarks')
replaces=('krunner-firefoxbookmarks')

build() {
  cd ${srcdir}/plasma-runner-browsefirefoxbookmarks/

  mkdir build
  cd build
  cmake ../ -DCMAKE_INSTALL_PREFIX=`kde4-config --prefix` || return 1
  make || return 1
}

package() {
  cd ${srcdir}/plasma-runner-browsefirefoxbookmarks/build

  make DESTDIR=$pkgdir install || return 1
}
