# Maintainer: Aldo Adirajasa Fathoni <aldo.alfathoni@gmail.com>
pkgname=ofonoctl
pkgver=0.4.1
pkgrel=3
pkgdesc="test/control application for the ofono daemon"
url="https://git.sr.ht/~martijnbraam/ofonoctl"
arch=("any")
license=("MIT")
depends=("python3" "python3-dbus" "python3-tabulate")
makedepends=("python3-setuptools")
source=("https://files.pythonhosted.org/packages/source/o/ofonoctl/ofonoctl-$pkgver.tar.gz")
sha512sums=("3bcdc56b9e5221052c40f4fc4836d0b781091ba28e04b267d403f72f297196fd71b059295431de0a0f09401deba6a867994899736bda631b8c86ddfbd845e7d1")

build() {
	cd "${pkgname}-${pkgver}"
	python3 setup.py build
}

package() {
	cd "${pkgname}-${pkgver}"
	python3 setup.py install --prefix=/usr --root="$pkgdir"
}
