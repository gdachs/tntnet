# Maintainer: Christopher Reimer <c[dot]reimer[at]googlemail[dot]com>
pkgname=tntnet
pkgver=2.1
pkgrel=2
pkgdesc="Modular, multithreaded, high performance webapplicationserver for C++"
url="http://www.tntnet.org"
arch=('x86_64' 'i686')
license=('GPL2')
depends=('cxxtools' 'openssl')
options=(!libtool)
source=("http://www.tntnet.org/download/${pkgname}-${pkgver}.tar.gz")
md5sums=('a9c85aa6d624f7f88c48374f28730242')

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  ./configure --prefix=/usr \
              --disable-unittest \
              --with-demos=no \
              --with-server=no
  make
}

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"

  make DESTDIR="${pkgdir}" install
}
