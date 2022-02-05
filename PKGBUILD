pkgname=c-oneliner
pkgver=0.0.5
pkgrel=1
pkgdesc="a one liner script to compile and run simple C/C++ programs"
arch=('any')
depends=('zsh' 'gcc')
url='https://github.com/aoaaceai/c-oneliner'
source=("$url/releases/download/v$pkgver/$pkgname-$pkgver.tar.gz")
license=('BSD')
sha256sums=('85b248343eb55cd9bf861e2f92a298c39531fb1cec4f16c853e57bc07a4bd709')

build() {
    cd "$pkgname-$pkgver"
    ./configure --prefix=/usr
}

package() {
    cd "$pkgname-$pkgver"
    make DESTDIR="$pkgdir/" install
    install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
