# Maintainer: anto22 <https://github.com/anto22>
pkgname=obs-plugin-countdown-bin
pkgver=2.1.1
pkgrel=1
pkgdesc="Countdown timer plugin for OBS Studio"
arch=('x86_64')
url="https://github.com/ashmanix/obs-plugin-countdown"
license=('GPL2')
depends=('obs-studio')
provides=("obs-plugin-countdown=${pkgver}")
conflicts=('obs-plugin-countdown' 'obs-countdown')

# ATTENTION : Vérifie que ce nom de fichier existe vraiment dans la release 2.1.1
source=("https://github.com/ashmanix/obs-plugin-countdown/releases/download/v${pkgver}/obs-plugin-countdown-${pkgver}-x86_64-linux-gnu.deb")
sha256sums=('01b623173f68acc989c851252cdd53e427d759826b46abfc3203033d1f9da501')

package() {
    bsdtar -xf "${srcdir}/data.tar.gz" -C "${pkgdir}/"

    # Nettoyage du dossier inutile
    cd "${pkgdir}/usr/lib"
    if [ -d "x86_64-linux-gnu/obs-plugins" ]; then
        mv x86_64-linux-gnu/obs-plugins .
        rm -rf x86_64-linux-gnu
    fi

    chown -R root:root "${pkgdir}/"
}
