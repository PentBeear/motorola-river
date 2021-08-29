# Reference: <https://postmarketos.org/devicepkg>
pkgname=device-motorola-river
pkgdesc="Motorola Moto G7"
pkgver=4.9.206
pkgrel=0
url="https://postmarketos.org"
license="MIT"
arch="aarch64"
options="!check !archcheck"
depends="
	linux-motorola-river
	mesa-dri-gallium
	mkbootimg
	postmarketos-base
"
makedepends="devicepkg-dev"
source="deviceinfo initfs-hook.sh"
subpackages="$pkgname-nonfree-firmware:nonfree_firmware"

build() {
	devicepkg_build $startdir $pkgname
}

package() {
	devicepkg_package $startdir $pkgname
}

nonfree_firmware() {
	pkgdesc="Wifi firmware"
	depends="firmware-motorola-river"
	mkdir "$subpkgdir"
}


sha512sums="
c9e5274c8b43701e8c56053239bcf8fe5028fcd4e52a4d7333209609288cb67f50520048ff0188edccc857c68f32908061cd957cfba537534095c67f11b785c0  deviceinfo
0dac3c9e032e41ecc81dc1a662e6bb9ee3aeb9cd6a5443ec071e6451561d7ae17366cc9546143a05cc7bc1535f7532b943db8521320cb52b7908f205fa4c9c25  initfs-hook.sh
"
