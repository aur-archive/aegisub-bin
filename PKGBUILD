# Maintainer: Kozec <kozec at kozec dot com>

pkgname=aegisub-bin
pkgver=2.1.9
pkgrel=1
pkgdesc="A general-purpose subtitle editor with ASS/SSA support (unofficial pre-compiled binaries)"
arch=('i686' 'x86_64')
url="http://www.aegisub.net/"

license=('GPL' 'BSD')
provides=('aegisub')
conflicts=('aegisub' 'aegisub-svn' 'aegisub-stable-svn')
source=("http://dl.dropbox.com/u/134520/aegisub-precompiled-${pkgver}.tar.gz")

# Dependencies converted from 'Building Aegisub 2.1.9 on Ubuntu' thread,
# http://forum.aegisub.org/viewtopic.php?f=10&t=4686
depends=('imagemagick' 'gcc-libs>=4.5' 'fontconfig' 'freetype2' 'libgl'
		'mesa' 'glib2' 'lua>=5.0' 'hunspell' 'alsa-lib' 'libpulse'
		'wxgtk>=2.8' 'libass' 'ffmpeg>=20120127' 'ffmpegsource>=2.0')
# excluded dep: openal 


build() {
	true
}

package() {
	cd "$srcdir/"
	mkdir -p $pkgdir/usr/bin
	cp -R "share" $pkgdir/usr
	cp bin/aegisub-2.1-${CARCH} $pkgdir/usr/bin/aegisub-2.1
	ln -s aegisub-2.1 $pkgdir/usr/bin/aegisub
}

md5sums=('3c6f10d88003970bc2d80ecce49c7302')
