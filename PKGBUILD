# Maintainer: loh.tar <loh.tar at googlemail dot com>
pkgname='tbsm-xinitrc'
pkgparent='tbsm'
pkgver='0.5'
pkgrel='1'
pkgdesc='A pure bash session or application launcher. Inspired by cdm, tdm and krunner.'
arch=('any')
url='https://github.com/loh-tar/tbsm'
license=('GPL')
depends=('bash')
backup=("etc/xdg/$pkgparent/$pkgparent.conf")
install="$pkgparent.install"
source=("$pkgname-$pkgver.tar.gz::https://github.com/loh-tar/$pkgparent/archive/v$pkgver.tar.gz"
        "tbsm_xinitrc.patch")
md5sums=('35faadd3c3cdba0c87541823cadb65f1'
         'fe7f5508ca705e5d80d456f9ee51de5c')

package() {
  cd "$pkgparent-$pkgver"
  patch --forward --strip=1 --input="${srcdir}/tbsm_xinitrc.patch"
  make install DESTDIR="$pkgdir"
}
