# Maintainer: Stefan Auditor <stefan.auditor@erdfisch.de>
# Contributor: Marc Straube <email@marcstraube.de>
# Contributor: Attila Bukor <r1pp3rj4ck [at] w4it [dot] eu>
# Please report issues at https://github.com/sanduhrs/arch-aur-phpunit

_pkgname=phpunit
pkgname=${_pkgname}
pkgver=9.3.2
pkgrel=1
pkgdesc="PHPUnit is a programmer-oriented testing framework for PHP."
url="https://phpunit.de"
arch=("any")
license=("BSD")
depends=("php>=7.0.0")
install="${_pkgname}.install"
source=("https://phar.phpunit.de/phpunit-${pkgver}.phar"
        "https://raw.githubusercontent.com/sebastianbergmann/phpunit/${pkgver}/LICENSE")
sha512sums=('ce5ab75ec8749986e37b767e6a3e2cee7d74d65599f92ef39a5c72e26225e60604429c6538473a03c0a6ad4fa9535d301b3e34432456f376bf43772cb8ffea94'
            '9ca5ce5d441629921af418c7d700d3a6942fbaa07d0081ce5abf835122f2f025b7737daedf55b2039d05875dac4d09fc034ea3dbd97404d8d1f326b1ce7b22df')

package() {
  install -D -m 644 "${srcdir}/LICENSE" "${pkgdir}/usr/share/licenses/${_pkgname}/LICENSE"
  install -D -m 755 "${srcdir}/${_pkgname}-${pkgver}.phar" "${pkgdir}/usr/share/webapps/bin/${_pkgname}.phar"
  install -d "${pkgdir}/usr/bin"
  ln -s "/usr/share/webapps/bin/${_pkgname}.phar" "${pkgdir}/usr/bin/${_pkgname}"
}
