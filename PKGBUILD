# Generated by gem2arch (https://github.com/anatol/gem2arch)
# Maintainer: Babken Vardanyan <483ken@gmail.com>

_gemname=metasploit_data_models
pkgname=ruby1.9-$_gemname
pkgver=0.19.4
pkgrel=1
pkgdesc='Database code for MSF and Metasploit Pro'
arch=(any)
url='http://www.metasploit.com/'
license=()
depends=(ruby1.9 ruby1.9-activerecord ruby1.9-activesupport ruby1.9-metasploit-concern ruby1.9-metasploit-model ruby1.9-arel-helpers ruby1.9-pg)
options=(!emptydirs)
source=(https://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha1sums=('02a04c24e1845c9a8a3867801f81a7772c811a2b')

package() {
  local _gemdir="$(ruby-1.9 -e'puts Gem.default_dir')"
  gem-1.9 install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" $_gemname-$pkgver.gem
  rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/LICENSE" "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
