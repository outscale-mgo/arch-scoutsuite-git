# Maintainer: Matthias gatto <matthias.gatto@outscale.com>
# Reference: PKGBUILD(5)

pkgname=scoutsuite-git
pkgver=0
pkgrel=1
pkgdesc='ScoutSuite is a security tool for cloud'

arch=('any')
url='https://github.com/nccgroup/ScoutSuite'
license=(GPL2)

source=("git://github.com/nccgroup/ScoutSuite.git")
sha256sums=("SKIP")

depends=(
	python-dateutil
	python-netaddr
	python-sqlitedict
	python-cherrypy
	python-cherrypy-cors
	python-coloredlogs
	python-asyncio-throttle
)

optdepends=(python-azure-cli)

build() {
        cd "${srcdir}/ScoutSuite"
        python ./setup.py build
}

package() {
        cd "${srcdir}/ScoutSuite"
        python  ./setup.py install --root="$pkgdir" --optimize=1 --skip-build
}