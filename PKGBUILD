# Maintainer: Jan Boelsche <jan@lagomorph.de>
pkgname=compiz-user-service
pkgver=1.2.0
pkgrel=1
pkgdesc="Run compiz as a (fake) systemd user service"
arch=('x86_64')
license=('GPL')
groups=()
depends=(
  'compiz-core'
  'background'
  'lightdm-autologin'
)
conflicts=(
  'launch-compiz'
)

source=(
  'kiosk-compiz.service'
  'compiz-do'
  'compiz-set-output-size'
  'compiz-get-output-size'
  '50-compiz'
)

sha256sums=('48f829c8eb77a952c55009dc45434b837b4ab0c540af9fb116a08c873e8eb5bd'
            'a0b75f3207857ac997a4be1f5d0c4582167a891c8ac81433d2ebddf41acffb7c'
            '29d0302ba452339372d6615ba4a36151c8b57fcaa7fa59bbd926fc89cc481de8'
            '7ec215a325ce8980f05606ade7b636c35ae3f797d6133bd64ccc1079bb8474ff'
            '8bf6cd37713d9e6ddbcfb10ecae2fc44e93f4b5cfedc498aa054e871ec61a1f0')

package () {
  install -Dm 755 -t "${pkgdir}/usr/bin" "compiz-do"
  install -Dm 755 -t "${pkgdir}/usr/bin" "compiz-set-output-size"
  install -Dm 755 -t "${pkgdir}/usr/bin" "compiz-get-output-size"
  install -Dm 644 -t "${pkgdir}/usr/lib/systemd/user" "kiosk-compiz.service"
  install -Dm 755 -t "${pkgdir}/home/auto-login/xsession.d" "50-compiz"
}
