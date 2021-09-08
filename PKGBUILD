pkgname=c-oneliner
pkgver=0.0.4
pkgrel=1
pkgdesc="a one liner script to compile and run simple C/C++ programs"
arch=('any')
depends=('zsh' 'gcc' 'aoaaceai-keyring')
url='https://github.com/aoaaceai/c-oneliner'
source=("$url/releases/download/v$pkgver/$pkgname-$pkgver.tar.gz")
license=('BSD')
sha256sums=('28ea6f338f8b3386198293e25c6096f7e88d7ecb9c489ad05629a6c8cf6ae852')

build() {
    cd "$pkgname-$pkgver"
    ./configure --prefix=/usr
}

package() {
    cd "$pkgname-$pkgver"
    make DESTDIR="$pkgdir/" install
    install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
