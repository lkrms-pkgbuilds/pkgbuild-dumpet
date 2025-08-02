# Maintainer: Luke Arms <luke@arms.to>
# Contributor: brent s. <bts[at]square-r00t[dot]net>

pkgname=dumpet
pkgver=2.1
pkgrel=8
commit=eca7061c2141885d64e1cbd72bec1faa73e6dbde
pkgdesc="Tool for debugging and verifying El Torito boot data on CD-like images"
arch=('i686' 'x86_64')
license=('GPL2')
url="https://github.com/rhboot/dumpet"
depends=('glibc' 'libxml2-legacy' 'popt')
source=("git+https://github.com/rhboot/${pkgname}.git#commit=${commit}")
sha256sums=('fbfeb6c5966d8826db7205487d1c3c2080be65468038806c5518937d094b5a85')

build() {
    cd "${srcdir}/${pkgname}"
    PKG_CONFIG_PATH=/usr/lib/libxml2-legacy/lib/pkgconfig make
}

package() {
    cd "${srcdir}/${pkgname}"
    make DESTDIR="${pkgdir}/" install
}
