pkgname=pymdown-extensions
pkgver=10.14
pkgrel=1
pkgdesc='Extensions for Python Markdown'
arch=('x86_64')
url="https://facelessuser.github.io/pymdown-extensions"
license=('MIT')
depends=('python3-markdown' 'python3-pygments')
makedepends=('python3-setuptools')
source=("https://github.com/facelessuser/${pkgname}/archive/refs/tags/${pkgver}.tar.gz")
sha256sums=('cff9df29d6f970fb5c364e0f5a857a83c43d5f37a38fd8a4349a9a5afb077cbe')

build() {
	cd "${pkgname}-${pkgver}"
	python3 -m build --wheel
}

package() {
	cd "${pkgname}-${pkgver}"
	python3 -m installer --destdir="$pkgdir" dist/*.whl
	install -Dm644 LICENSE.md -t "${pkgdir}/usr/share/licenses/${pkgname}"
}
