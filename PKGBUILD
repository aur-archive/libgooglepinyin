# Author: CSSlayer <wengxt@gmail.com>
# Maintainer: Yangtse <yangtsesu@gmail.com> 

pkgname=libgooglepinyin
pkgver=0.1.2
pkgrel=1
pkgdesc="A fork from google pinyin on android"
arch=('i686' 'x86_64')
url="http://code.google.com/p/libgooglepinyin"
license=('APACHE')
makedepends=('cmake')
conflicts=('libgooglepinyin-hg')
source=(http://libgooglepinyin.googlecode.com/files/${pkgname}-${pkgver}.tar.bz2)

build(){
  cd "${srcdir}"

  msg "Starting make..."

  rm -rf "${srcdir}/build"
  cp -rf "${srcdir}/${pkgname}-${pkgver}" "$srcdir/build"
  cd "${srcdir}/build"

  cmake -DCMAKE_INSTALL_PREFIX=/usr . \
      -DENABLE_STATIC=Off
  make DESTDIR=${pkgdir} install
}

md5sums=('d697aba08fdc0fe15c9d7b6096ca3b28')
