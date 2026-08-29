# Maintainer: anto22 <https://github.com/anto22>
pkgname=obs-plugin-countdown-bin
pkgver=2.2.0
pkgrel=1
pkgdesc="Countdown timer plugin for OBS Studio"
arch=('x86_64')
url="https://github.com/ashmanix/obs-plugin-countdown"
license=('GPL-2.0-or-later')
depends=('obs-studio')
provides=("obs-plugin-countdown=${pkgver}")
conflicts=('obs-plugin-countdown' 'obs-countdown')

source=("${pkgname}-${pkgver}.deb::https://github.com/ashmanix/obs-plugin-countdown/releases/download/${pkgver}/obs-plugin-countdown-${pkgver}-x86_64-linux-gnu.deb")
sha256sums=('a29790d93fb23f589688d9b196cfb174fed3aa92b109e0d31812a7bfa4b20e91')

package() {
    # Extraction du contenu du paquet Debian
    bsdtar -xf "${srcdir}/data.tar.xz" -C "${pkgdir}/" 2>/dev/null || bsdtar -xf "${srcdir}/data.tar.gz" -C "${pkgdir}/"

    # Déplacement des modules depuis la structure Debian/Ubuntu vers la structure Arch
    if [ -d "${pkgdir}/usr/lib/x86_64-linux-gnu/obs-plugins" ]; then
        mkdir -p "${pkgdir}/usr/lib/obs-plugins"
        mv "${pkgdir}/usr/lib/x86_64-linux-gnu/obs-plugins/"* "${pkgdir}/usr/lib/obs-plugins/"
        rm -rf "${pkgdir}/usr/lib/x86_64-linux-gnu"
    fi
}
