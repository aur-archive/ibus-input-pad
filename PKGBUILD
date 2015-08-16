# Maintainer: Limao Luo <luolimao+AUR@gmail.com>

pkgname=ibus-input-pad
pkgver=1.4.0
pkgrel=2
pkgdesc="Graphical tool to input special characters into text-based applications (IBus engine)"
arch=(i686 x86_64)
url=https://input-pad.googlecode.com
license=(LGPL)
depends=(ibus input-pad)
makedepends=(intltool)
source=($url/files/$pkgname-$pkgver.tar.gz)
sha256sums=('116bde32171325f80d3f58d3b0c3585662d306d9e257b3e853f071bcdce846a1')
sha512sums=('45eba131f6b387407f728e0851124c16821ca81e7d58aa3367f499e9abcfb23693515020bdcb3ae8b074ef9d374f4101de0f706484f547c8a0c70dd73b8931b9')

build() {
    cd "$srcdir"/$pkgname-$pkgver/
    ./configure --prefix=/usr --libexecdir=/usr/bin --enable-nls
    make
}

package() {
    cd "$srcdir"/$pkgname-$pkgver/
    make DESTDIR="$pkgdir" install
}
