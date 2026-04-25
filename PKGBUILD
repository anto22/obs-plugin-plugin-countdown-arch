# Maintainer: anto22 <https://github.com/anto22/>

pkgname=obs-plugin-plugin-countdown-bin
pkgver=2.1.1
pkgrel=2.1.1
arch=(x86_64)
pkgdesc="A countdown timer that displays the time using a text source"
url="https://github.com/ashmanix/obs-plugin-countdown"
license=('GPL2')
depends=("obs-studio")
provides=("obs-plugin-plugin-countdown=$pkgver")
conflicts=("obs-plugin-plugin-countdown" "obs-countdown")
source=("https://github.com/ashmanix/obs-plugin-countdown/releases/download/v$pkgver/obs-plugin-countdown-$pkgver-x86_64-linux-gnu.deb")
sha256sums=('01b623173f68acc989c851252cdd53e427d759826b46abfc3203033d1f9da501')

package() {
  bsdtar -xf ${srcdir}/data.tar.gz -C ${pkgdir}/
  cd ${pkgdir}/usr/lib/
  mv x86_64-linux-gnu/obs-plugins .
  rm -r x86_64-linux-gnu
  chown root:root -vR "${pkgdir}/"
}
