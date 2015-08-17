# Maintainer: Jimmy Mabey <jimmymabey@gmail.com>
# Contributor: kpdecker <kpdecker@gmail.com>
pkgname=nodejs-handlebars
pkgver=2.0.0
pkgrel=1
pkgdesc="Extension of the Mustache logicless template language"
arch=('any')
url="http://handlebarsjs.com"
license=('MIT')
depends=('nodejs')
changelog=$pkgname.changelog

build() {
  cd "$srcdir"

  mkdir -p "$srcdir/usr/lib/node_modules"
  npm install -g --prefix "$srcdir/usr" handlebars@$pkgver
}

package() {
  cd "$srcdir"

  cp -R usr "$pkgdir"
  install -D -m644 usr/lib/node_modules/handlebars/LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
