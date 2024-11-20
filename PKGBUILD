# Maintainer: anto22 <https://github.com/anto22/>

pkgname=obs-plugin-plugin-countdown-bin
pkgver=1.3.3
pkgrel=1
arch=(x86_64)
pkgdesc="A countdown timer that displays the time using a text source"
url="https://github.com/ashmanix/obs-plugin-countdown"
license=('GPL2')
depends=("obs-studio")
provides=("obs-plugin-plugin-countdown=$pkgver")
conflicts=("obs-plugin-plugin-countdown" "obs-countdown")
source=("https://github.com/ashmanix/obs-plugin-countdown/releases/download/v$pkgver/obs-plugin-countdown-$pkgver-linux-x86_64.deb")
sha256sums=('2860b02381bfad36b77d0ddbda1543ad7de64344ce37decc0b26bc603685f19c')

package() {
  bsdtar -xf ${srcdir}/data.tar.gz -C ${pkgdir}/
  cd ${pkgdir}/usr/lib/
  mv x86_64-linux-gnu/obs-plugins .
  rm -r x86_64-linux-gnu
  chown root:root -vR "${pkgdir}/"
}
