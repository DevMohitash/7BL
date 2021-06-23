# Maintainer:

pkgname=mkadp-git
pkgver=1.0.ac279a9
pkgrel=1
pkgdesc="ButterLimits - Blah Blah Blah!!!"
arch=('any')
url="https://github.com/DevMohitash/7BL.git"
license=('GPL3')
depends=()
makedepends=('git')
source=("$pkgname"::'git+https://github.com/DevMohitash/mkadp')
md5sums=('SKIP')
provides=(mkadp)

pkgver() {
  cd "$pkgname"
  echo "1.0.`git rev-parse --short HEAD`"
}

package() {
  cd "$srcdir/${pkgname}/"
  chmod +x mkadp
  mkdir -p "$pkgdir/usr/bin/"
  mkdir -p "$pkgdir/etc/systemd/system/"
  install -Dm744 ktweak "$pkgdir/usr/bin/mkadp"
  install -Dm644 ktweak.service "$pkgdir/etc/systemd/system/mkadp.service"
}
