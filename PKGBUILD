pkgname=pymdown-extensions
pkgver=10.7.1
pkgrel=1
pkgdesc='Extensions for Python Markdown'
arch=('x86_64')
url="https://facelessuser.github.io/pymdown-extensions"
license=('MIT')
depends=('python3-markdown' 'python3-pygments')
makedepends=('python3-setuptools')
source=("https://github.com/facelessuser/${pkgname}/archive/refs/tags/${pkgver}.tar.gz")
sha256sums=('a9f0123f3fa7934c61847644e752772147d1f5aed0f692f99455d9e9b50b336e')

build() {
	cd "${pkgname}-${pkgver}"
	python3 -m build --wheel
}

package() {
	cd "${pkgname}-${pkgver}"
	python3 -m installer --destdir="$pkgdir" dist/*.whl
	install -Dm644 LICENSE.md -t "${pkgdir}/usr/share/licenses/${pkgname}"
}
sha256sums=('065d6a7844b79d729a52e02717a79309b45158904b305c5fa350266e5256b59b')
