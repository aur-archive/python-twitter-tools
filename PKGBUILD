# Maintainer: Dennis Fink <dennis.fink@c3l.lu>

pkgname=python-twitter-tools
pkgver=1.14.2
pkgrel=1
pkgdesc="An API and command-line toolset for Twitter (twitter.com)"
arch=('any')
url="http://pypi.python.org/pypi/twitter/"
license=('MIT')
depends=('python')
makedepends=('python-setuptools')
source=("http://pypi.python.org/packages/source/t/twitter/twitter-${pkgver}.tar.gz" "LICENSE")
md5sums=('7eec6f1b6b178eaefe05de1a3da1090e'
         'a5da3e25967f8405eb578fa3ab7f4098')
conflicts=('python-twitter-tools-git')

build() {

  cd "$srcdir/twitter-$pkgver"
  python setup.py build

}

package() {

  cd "$srcdir/twitter-$pkgver"
  python setup.py install --root=$pkgdir --optimize=1

  install -D -m644 $srcdir/LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"

}

# vim:set ts=2 sw=2 et:
