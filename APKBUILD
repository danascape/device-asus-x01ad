# Reference: <https://postmarketos.org/devicepkg>
pkgname=device-asus-x01ad
pkgdesc="Asus Max M2"
pkgver=1
pkgrel=0
url="https://postmarketos.org"
license="MIT"
arch="aarch64"
options="!check !archcheck"
depends="
	linux-postmarketos-qcom-msm8953
	mesa-dri-gallium
	msm-fb-refresher
	mkbootimg
	postmarketos-base
"
makedepends="devicepkg-dev"
subpackages="$pkgname-nonfree-firmware:nonfree_firmware"
source="deviceinfo"

build() {
	devicepkg_build $startdir $pkgname
}

package() {
	devicepkg_package $startdir $pkgname
}

nonfree_firmware() {
	pkgdesc="Wi-Fi, ADSP Firmware"
	depends="firmware-asus-x01ad"
	mkdir "$subpkgdir"
}

sha512sums="
31f82f855e0dbf5f701ee9bb92e10387d5c03cc9ffc43fa1880b6b10336f0bb8442f1bc9a4889ba9bfeae25df94999c009ca54235a2153d5e94f2fcf2f31f34c  deviceinfo
"
