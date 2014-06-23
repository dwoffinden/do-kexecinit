# do-kexecinit PKGBUILD
#
# Maintainer Brian Parsons <brian@pmex.com>
#

pkgname=do-kexecinit
pkgver=1.1
pkgrel=1
pkgdesc="init replacement bootloader for Digital Ocean"
arch=('any')
license=('MIT')
depends=('kexec-tools' 'linux-lts' 'systemd')
conflicts=('systemd-sysvcompat')
source=('init' 
        'LICENSE')
md5sums=('f691995b211154a65e33905682fe029e'
         '62ce522f205ff9f66b3aa6fbb8f10311')

package() {

    install -D -m 755 "${srcdir}/init" "${pkgdir}/usr/bin/init"

    for tool in runlevel reboot shutdown poweroff halt telinit
    do
        ln -s systemctl "${pkgdir}/usr/bin/${tool}"
    done

    install -Dm 755 "${srcdir}/LICENSE" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"

}

