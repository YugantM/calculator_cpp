pkgname=calculator_cpp
pkgver=0.0.1
pkgrel=1
pkgdesc="a small C++ project to show CMake, calculator_cpp uses a library to calculate something out of 2 integers"
arch=('i686' 'x86_64' 'armv7h')
url="https://github.com/majorx234/calculator"
license=('GPLv2')
depends=('libadd_cpp')
makedepends=('cmake' 'git')
_dir=${pkgname}
source=("${_dir}"::"git+https://github.com/majorx234/calculator_cpp.git")
md5sums=('SKIP')

build() {
  # Create build directory
  [ -d ${srcdir}/build ] || mkdir ${srcdir}/build
  cd ${srcdir}/build

  cmake ${srcdir}/$pkgname \
        -DCMAKE_INSTALL_PREFIX=/usr 
  make 
}

package() {
   cd "${srcdir}/build"
   make DESTDIR="$pkgdir/" install
}

# vim:set ts=2 sw=2 et:

