pkgname=c-oneliner
pkgver=0.0.3
pkgrel=1
pkgdesc="a one liner script to compile and run simple C/C++ programs."
arch=('any')
depends=('zsh')
source=("https://github.com/aoaaceai/c-oneliner/releases/download/v$pkgver/$pkgname-$pkgver.tar.gz")
license=('BSD')
sha256sums=('8d017da3d33ffca248d5dc3acf9c216ee443aebc82e08224adf37f313bbdace7')

build() {
    cd "$pkgname-$pkgver"
    ./configure --prefix=/usr
}

package() {
    cd "$pkgname-$pkgver"
    make DESTDIR="$pkgdir/" install
    install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
