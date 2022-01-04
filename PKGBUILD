_pkgname=dmenu
pkgname=$_pkgname-git
pkgver=5.0
pkgrel=1
pkgdesc="A generic menu for X"
url="http://tools.suckless.org/dmenu/"
arch=('i686' 'x86_64')
license=('MIT')
depends=('sh' 'libxinerama' 'libxft')
makedepends=('git')
provides=($_pkgname)
conflicts=($_pkgname)
source=('arg.h' 'config.h' 'config.mk' 'dmenu.1' 'dmenu.c'
    'dmenu_path' 'dmenu_run' 'drw.c' 'drw.h' 'LICENSE'
    'Makefile' 'stest.1' 'stest.c' 'util.c' 'util.h')
md5sums=('SKIP' 'SKIP' 'SKIP' 'SKIP' 'SKIP'
    'SKIP' 'SKIP' 'SKIP' 'SKIP' 'SKIP' 
    'SKIP' 'SKIP' 'SKIP' 'SKIP' 'SKIP')

build(){
  make PREFIX=/usr DESTDIR="$pkgdir"
}

package() {
  make PREFIX=/usr DESTDIR="$pkgdir" install
  install -Dm644 LICENSE "$pkgdir"/usr/share/licenses/$pkgname/LICENSE
}
