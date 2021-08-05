pkgname=c-oneliner
pkgver=0.0.1
pkgrel=1
pkgdesc="a one liner script to compile and run simple C/C++ programs."
arch=('any')
depends=('gcc' 'zsh')
source=("https://github.com/aoaaceai/c-oneliner/releases/download/v$pkgver/$pkgname-$pkgver.tar.gz")
license=('BSD')
sha256sums=('f575b2ddce8680f06b77a46af65470d82e99644b48f952c1ada3f96b9e66ab1a')

package() {
    cd "$pkgname-$pkgver"
    ls > /tmp/ls
}
