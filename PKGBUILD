# Maintainer: twa022 <twa022 at gmail dot com>

_pkgname=asterisk
pkgname=${_pkgname}
pkgver=21.0.0
pkgrel=1
pkgdesc='Asterisk, a server for SIP and RTP applications.'
arch=('x86_64')
url='http://www.github.com/bcsmith2846/asterisk'
license=('GPL2')
depends=('zlib' 'jansson' 'speex' 'speexdsp' 'unixodbc' 'curl' 'libcurl-gnutls' 'libvorbis' 'libogg' 'libsrtp' 'libical' 'neon' 'gmime3' 'unbound' 'libxml2' 'util-linux-libs' 'openssl' 'libxslt' 'sqlite' 'libresample' 'pjproject')
makedepends=('base-devel' 'ncurses' 'glibc')
provides=("${_pkgname}")
conflicts=("${_pkgname}")
source=()
sha256sums=('SKIP')

build() {
  cd $srcdir/..
  make -j20
}

package() {
  cd $srcdir/..
  make DESTDIR="${pkgdir}/" install 
  make -j20 DESTDIR="${pkgdir}/" progdocs 
  make DESTDIR="${pkgdir}/" samples
}
