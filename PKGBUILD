pkgname=c-oneliner
pkgver=0.0.2
pkgrel=1
pkgdesc="a one liner script to compile and run simple C/C++ programs."
arch=('any')
depends=('zsh')
source=("https://github.com/aoaaceai/c-oneliner/releases/download/v$pkgver/$pkgname-$pkgver.tar.gz")
license=('BSD')
sha256sums=('9578008c98b51835b17435988c5e2c707d52e588f66ddce3adb720e9fa4e7b2d')

build() {
    cd "$pkgname-$pkgver"
    ./configure --prefix=/usr
}

package() {
    cd "$pkgname-$pkgver"
    make DESTDIR="$pkgdir/" install
    install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
