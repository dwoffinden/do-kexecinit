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
depends=('kexec-tools' 'linux-lts' 'systemd')
conflicts=('systemd-sysvcompat')
source=('init' 'LICENSE')
md5sums=('f691995b211154a65e33905682fe029e'
         'c3915f6ecafdbe5d0660b4b59cc01eed')

package() {

    install -D -m 755 ${srcdir}/init ${pkgdir}/usr/bin/init

    install -dm755 "$pkgdir/usr/bin"
    for tool in runlevel reboot shutdown poweroff halt telinit; do
        ln -s 'systemctl' "$pkgdir/usr/bin/$tool"
    done

    install -Dm 755 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
