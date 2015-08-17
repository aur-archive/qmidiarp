# Maintainer : speps <speps at aur dot archlinux dot org>
# Contributor: Shinlun Hsieh <yngwiexx@yahoo.com.tw>

pkgname=qmidiarp
pkgver=0.6.0
pkgrel=1
pkgdesc="A MIDI arpeggiator, phrase generator and controller LFO for the ALSA sequencer."
arch=(i686 x86_64)
url="http://sourceforge.net/projects/qmidiarp/"
license=('GPL')
depends=('qt4' 'jack' 'liblo' 'lv2')
install="$pkgname.install"
source=("http://downloads.sourceforge.net/project/$pkgname/$pkgname/$pkgver/$pkgname-$pkgver.tar.bz2")
md5sums=('3315ca9f9cc8964706b5b8e8e85a09b9')

build() {
  cd $pkgname-$pkgver
  ./configure --prefix=/usr
  make
}

package() {
  cd $pkgname-$pkgver
  make DESTDIR="$pkgdir/" install
}
