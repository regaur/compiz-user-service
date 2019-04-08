# Maintainer: Jan Boelsche <jan@lagomorph.de>
pkgname=compiz-user-service
pkgver=1.0.0
pkgrel=2
pkgdesc="Run compiz as a systemd user service"
arch=('x86_64')
license=('GPL')
groups=()
depends=(
  'compiz-core'
  'background'
)
conflicts=(
  'launch-compiz'
)

source=(
  'kiosk-compiz.service'
  'compiz-do'
  'compiz-set-output-size'
  'compiz-get-output-size'
)

sha256sums=('3171792613770c0489a0d5d13eb0bc3f195b4099bc71882707a34d3c9f174d7e'
            'a0b75f3207857ac997a4be1f5d0c4582167a891c8ac81433d2ebddf41acffb7c'
            '29d0302ba452339372d6615ba4a36151c8b57fcaa7fa59bbd926fc89cc481de8'
            '7ec215a325ce8980f05606ade7b636c35ae3f797d6133bd64ccc1079bb8474ff')

package () {
  install -Dm 755 -t "${pkgdir}/usr/bin" "compiz-do"
  install -Dm 755 -t "${pkgdir}/usr/bin" "compiz-set-output-size"
  install -Dm 755 -t "${pkgdir}/usr/bin" "compiz-get-output-size"
  install -Dm 644 -t "${pkgdir}/usr/lib/systemd/user" "kiosk-compiz.service"
}
