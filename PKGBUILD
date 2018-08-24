# Maintainer: Justin Wong <justin.w.xd at gmail dot com>
# Co-Maintainer: Peter Cai <peter at typeblog dot net>
_distro="ubuntu"

pkgname=netease-cloud-music
pkgver=1.1.0
pkgrel=1
pkgdesc="Netease Cloud Music, converted from .deb package"
arch=("x86_64")
url="http://music.163.com/"
license=('custom')
depends=(
	"alsa-lib" "gtk2" "nss" "libxss"
	"qt5-multimedia" "qt5-x11extras"
	"gst-libav" "gst-plugins-base"
	"gst-plugins-good" "gst-plugins-ugly"
	"gnome-themes-standard" "gconf" "atk"
	"glibc" "cairo" "vlc" "fontconfig"
	"dbus" "cups" "expat" "gdk-pixbuf2"
	"glib2" "pango" "libpulse" "sqlite"
	"gcc-libs" "libx11" "zlib"
)
source=(
	"http://d1.music.126.net/dmusic/${pkgname}_${pkgver/_/-}_amd64_${_distro}.deb"
	"http://music.163.com/html/web2/service.html"
)
md5sums=('a678960abf7b83ac89eb9a034a580e8a'
         'SKIP')

package() {
  cd ${srcdir}
  tar -xvf data.tar.xz -C ${pkgdir}
  install -D -m644 service.html ${pkgdir}/usr/share/licenses/$pkgname/license.html
}
