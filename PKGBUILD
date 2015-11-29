pkgname=ois
pkgver=1.3.80
_commit=bb75ccc1aabc1c547195579963601ff6080ca2f2
pkgrel=1
pkgdesc="Object Oriented Input System"
url="https://github.com/wgois/OIS"
arch=('x86_64')
license=('GPL2')
makedepends=('autoconf' 'automake' 'libtool' 'gcc' 'libxaw')
source=("https://github.com/wgois/OIS/archive/${_commit}.zip")
md5sums=('92aff7d696a1246471d20d846b945a7c')

build() {
  cd ${srcdir}/OIS-${_commit}
  chmod +x bootstrap
  ./bootstrap
  ./configure --prefix=/usr
  make
}

package() {
  cd ${srcdir}/OIS-${_commit}
  make DESTDIR=${pkgdir} install
}
