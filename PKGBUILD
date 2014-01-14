# Maintainer: DavidK <david_king at softhome dot net>
# Contributor: Laszlo Papp <djszapi @ gmail at com>
# Contributor: chenss <ufbycd@163.com>

pkgname=cgic-git
pkgver=20140114
pkgrel=1
pkgdesc="An ANSI C library for CGI Programming"
arch=('i686' 'x86_64')
url="https://github.com/ufbycd/cgic"
license=('GPL')
depends=('glibc')
makedepends=('git')
provides=('cgic')
conflicts=('cgic')
source=("git+https://github.com/ufbycd/cgic.git")
md5sums=('SKIP')

build() {
  cd "$srcdir/cgic"
  make || return 1
}

package() {
  cd "$srcdir/cgic"
  install -Dm755 cgictest.cgi ${pkgdir}/usr/bin/cgictest.cgi || return 1
  install -Dm755 capture ${pkgdir}/usr/bin/capture || return 1
  install -Dm755 cgic.h ${pkgdir}/usr/include/cgic.h || return 1
  install -Dm755 libcgic.a ${pkgdir}/usr/lib/libcgic.a || return 1
}
