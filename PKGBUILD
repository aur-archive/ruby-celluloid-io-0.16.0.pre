# Generated by gem2arch (https://github.com/anatol/gem2arch)
# Maintainer: Anatol Pomozov <anatol.pomozov@gmail.com>

_gemname=celluloid-io
pkgname=ruby-$_gemname-0.16.0.pre
pkgver=0.16.0
pkgrel=1
pkgdesc='Celluloid::IO allows you to monitor multiple IO objects within a Celluloid actor'
arch=(any)
url='http://github.com/celluloid/celluloid-io'
license=(MIT)
depends=(ruby ruby-celluloid ruby-nio4r)
options=(!emptydirs)
source=(https://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha1sums=('c07f8f105652f5a978feabed38704ef2cffb07b8')

package() {
  local _gemdir="$(ruby -e'puts Gem.default_dir')"
  gem install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" -n "$pkgdir/usr/bin" $_gemname-$pkgver.gem
  rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/LICENSE.txt" "$pkgdir/usr/share/licenses/$pkgname/LICENSE.txt"
}
