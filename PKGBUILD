# Maintainer: mrjk <mrjk.78@gmail.com>

pkgname=libgnomekbd-viewer
pkgver=20170403
pkgrel=1
pkgdesc="Allow to show the current keyboard layout map with the gkbd-keyboard-display Gnome utiliy"
arch=('i686' 'x86_64')
license=('GPL')
url="https://github.com/mrjk/libgnomekbd-viewer.git"
provides=('libgnomekbd-viewer')
conflicts=('libgnomekbd-viewer')
depends=('xkblayout-state'
	 'libgnomekbd')
makedepends=()
source=('git+https://github.com/mrjk/libgnomekbd-viewer.git')
md5sums=('SKIP')

_gitname="libgnomekbd-viewer"
_gitbranch="master"

pkgver() {
  cd "$_gitname"
  git show -s --format="%ci" HEAD | sed -e 's/-//g' -e 's/ .*//'
}

package() {
  cd "$_gitname"
  install -Dm755 "gkbd-keyboard-display-current" "$pkgdir/usr/bin/gkbd-keyboard-display-current"  
  install -D "gkbd-keyboard-display-current.desktop" "$pkgdir/usr/share/applications/gkbd-keyboard-display-current.desktop"
}
