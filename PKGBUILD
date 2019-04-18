# Maintainer: Jan Boelsche <jan@lagomorph.de>
pkgname=compiz-user-service
pkgver=1.4.0
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

sha256sums=('893491401e467ecff86618f3edca6fcea22b8237c995732cadaccfd104c45406'
            'a0b75f3207857ac997a4be1f5d0c4582167a891c8ac81433d2ebddf41acffb7c'
            '29d0302ba452339372d6615ba4a36151c8b57fcaa7fa59bbd926fc89cc481de8'
            '7ec215a325ce8980f05606ade7b636c35ae3f797d6133bd64ccc1079bb8474ff'
            '9c4a751ef38ecbb5652666678badf6eb0315f674844967218bcfd009a5c5bbd7')

package () {
  install -Dm 755 -t "${pkgdir}/usr/bin" "compiz-do"
  install -Dm 755 -t "${pkgdir}/usr/bin" "compiz-set-output-size"
  install -Dm 755 -t "${pkgdir}/usr/bin" "compiz-get-output-size"
  install -Dm 644 -t "${pkgdir}/usr/lib/systemd/user" "kiosk-compiz.service"
  install -Dm 755 -t "${pkgdir}/home/auto-login/xsession.d" "50-compiz"
}
