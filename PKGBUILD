_pkgname=vim-ansible-yaml
pkgname=vim-ansible-yaml-git
pkgver=1405775142
pkgrel=1
pkgdesc="plugin for writing and editing documents in ansible's extended yaml"
arch=('any')
url='https://github.com/chase/vim-ansible-yaml'
license=('unknown')
depends=('vim')
makedepends=('git')
provides=('vim-ansible-yaml')
conflicts=('vim-ansible-yaml')

source=('git://github.com/chase/vim-ansible-yaml.git')
sha512sums=('SKIP')

pkgver() {
  cd -- "$srcdir/$_pkgname"
  git log -n1 --pretty=format:%ct
}

package() {
  cd "$srcdir/$_pkgname"
  install -dm755 "$pkgdir/usr/share/vim/vimfiles"
  find * -maxdepth 0 -type d -exec cp -R -t "$pkgdir/usr/share/vim/vimfiles" '{}' \+
}

