# Maintainer:     Cassidy Wilson <cassidywilson at mailbox dot org>	

pkgname=doomrunner
pkgver=1.3.3
pkgrel=1
pkgdesc="A ZDoom launcher using Qt"
arch=('x86_64')
url="https://github.com/Youda008/DoomRunner"
license=('GPL3')
depends=('qt5-base')
makedepends=('git')
source=("https://github.com/Youda008/DoomRunner/archive/v${pkgver}.tar.gz")
md5sums=('2cbafa2be376257c165ec4fc0f4ba9eb')

build() {
	mkdir -p "${srcdir}/DoomRunner-${pkgver}/build-dynamic"
	cd "${srcdir}/DoomRunner-${pkgver}/build-dynamic"
	qmake ../DoomRunner.pro -spec linux-g++ "CONFIG+=release"
	make	
}

package() {
	cd "${srcdir}/DoomRunner-${pkgver}/build-dynamic"
	make install INSTALL_ROOT="${pkgdir}/" 
}

