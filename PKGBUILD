pkgname=qogir-icon-theme-git
pkgver=2020.11.22.r8.g2944d3df
pkgrel=1
pkgdesc='A colorful design icon theme for linux desktops'
arch=('any')
url='https://github.com/vinceliuice/Qogir-icon-theme'
license=('GPL3')
depends=()
makedepends=('git')
optdepends=()
provides=('qogir-icon-theme')
conflicts=('qogir-icon-theme')
options=('!strip')
source=('git+https://github.com/vinceliuice/Qogir-icon-theme')
sha256sums=('SKIP')

pkgver() {
    cd Qogir-icon-theme
    git describe --long --tags | sed 's/\([^-]*-g\)/r\1/;s/-/./g'
}

package() {
    cd Qogir-icon-theme
    mkdir -p "${pkgdir}/usr/share/icons"
    ./install.sh -d "${pkgdir}/usr/share/icons"
    rm -rf "${pkgdir}/usr/share/icons/Qogir-manjaro"
    rm -rf "${pkgdir}/usr/share/icons/Qogir-manjaro-dark"
    rm -rf "${pkgdir}/usr/share/icons/Qogir-ubuntu"
    rm -rf "${pkgdir}/usr/share/icons/Qogir-ubuntu-dark"
}
