# Maintainer: David Phillips <dbphillipsnz at _remove this part if you want_ gmail dot com>

_gitowner=defuse
pkgname=passgen
pkgver=1.1
pkgrel=2
pkgdesc="A command-line password generator"
arch=('i686' 'x86_64')
url="https://github.com/${_gitowner}/${pkgname}/"
license=('GPL')
source=("${pkgname}-${pkgver}.tar.gz::https://github.com/${_gitowner}/${pkgname}/archive/v${pkgver}.tar.gz")
sha512sums=('cba54500e784750efcdabb7f4e359c41deb805a5113a6e1ce89de6d77eb12bfcf3b9b9d4e6048406a9f328ce7fb0f37f6c9bf9329020a50e8804d18497d5c6d0')

build () {
	make passgen --directory="${srcdir}/${pkgname}-${pkgver}"
}

package () {
	cd "${srcdir}/${pkgname}-${pkgver}"
	install -Dm 755 passgen "${pkgdir}/usr/bin/passgen"
}
