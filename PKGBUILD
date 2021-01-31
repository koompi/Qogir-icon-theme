pkgname=qogir-icon-theme-koompi
pkgver=20210131
pkgrel=1
pkgdesc='A colorful design icon theme for linux desktops'
arch=('any')
url='https://github.com/koompi/Qogir-icon-theme'
license=('GPL3')
depends=()
makedepends=('git')
optdepends=()
provides=('qogir-icon-theme')
conflicts=('qogir-icon-theme')
options=('!strip')
source=('git+https://github.com/koompi/Qogir-icon-theme.git')
sha256sums=('SKIP')

package() {
    cd Qogir-icon-theme
    git checkout koompi
    mkdir -p "${pkgdir}/usr/share/icons"
    ./install.sh -d "${pkgdir}/usr/share/icons"
    rm -rf "${pkgdir}/usr/share/icons/Qogir-manjaro"
    rm -rf "${pkgdir}/usr/share/icons/Qogir-manjaro-dark"
    rm -rf "${pkgdir}/usr/share/icons/Qogir-ubuntu"
    rm -rf "${pkgdir}/usr/share/icons/Qogir-ubuntu-dark"
    cp ${srcdir}/Qogir-icon-theme/koompi/koompi-white.svg ${pkgdir}/usr/share/icons/Qogir/scalable/apps/start-here-kde.svg
    cp ${srcdir}/Qogir-icon-theme/koompi/koompi-white.svg ${pkgdir}/usr/share/icons/Qogir/16/places/start-here-kde.svg
    cp ${srcdir}/Qogir-icon-theme/koompi/koompi-black.svg ${pkgdir}/usr/share/icons/Qogir-dark/16/places/start-here-kde.svg
}
