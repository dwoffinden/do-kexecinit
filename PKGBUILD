# do-kexecinit PKGBUILD
#
# Maintainer Brian Parsons <brian@pmex.com>
#

pkgname=do-kexecinit
pkgver=1.0
pkgrel=2
pkgdesc="init replacement bootloader for Digital Ocean"
arch=('any')
license=('MIT')
depends=('kexec-tools' 'linux-lts')
conflicts=('systemd-sysvcompat')
source=(init)
md5sums=('f691995b211154a65e33905682fe029e')

package() {

    install -D -m 755 ${srcdir}/init ${pkgdir}/usr/bin/init

}
