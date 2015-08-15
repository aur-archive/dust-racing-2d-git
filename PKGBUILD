pkgname=dust-racing-2d-git
_pkgname=DustRacing2D
pkgver=1.11.0.4f8ccb8
pkgrel=3
pkgdesc="Dust Racing 2D is a traditional top-down car racing game including a level editor."
url="https://github.com/juzzlin/DustRacing2D"
arch=('x86_64' 'i686')
license=('GPLv3')
depends=('qt5-base' 'openal' 'libvorbis' 'pkg-config')
source="git://github.com/juzzlin/$_pkgname.git"
conflicts=('dustrac')
md5sums=('SKIP')

build() {
    cd "$srcdir/$_pkgname"

    ./configure -DReleaseBuild=1 -DCMAKE_INSTALL_PREFIX=$_pkgname/usr
    make
}

package() {
    cd "$srcdir/$_pkgname"
    make INSTALL_ROOT="${pkgdir}" install
} 