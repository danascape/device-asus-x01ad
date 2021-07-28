# Reference: <https://postmarketos.org/devicepkg>
pkgname=device-asus-x01ad
pkgdesc="Asus Max M2"
pkgver=0.1
pkgrel=0
url="https://postmarketos.org"
license="MIT"
arch="aarch64"
options="!check !archcheck"
depends="
	linux-asus-x01ad
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

sha512sums="(run 'pmbootstrap checksum device-asus-x01ad' to fill)"
