# Maintainer: Alexey Yakovenko <waker@users.sourceforge.net>

pkgname=deadbeef
pkgver=0.4.2
pkgrel=2
pkgdesc="mp3/ogg/flac/ape/sid/mod/nsf/m4a/mpc/shn music player based on GTK2"
arch=(i686 x86_64)
url="http://deadbeef.sourceforge.net"
license=('GPL2')
makedepends=('gtk2', 'libsamplerate', 'libvorbis', 'libmad', 'flac', 'curl', 'alsa-lib', 'wavpack', 'libsndfile', 'libcdio', 'libcddb', 'ffmpeg', 'libx11', 'faad2', 'zlib', 'intltool', 'pkgconfig')
depends=('gtk2' 'libsamplerate' 'alsa-lib')
optdepends=('libvorbis: ogg vorbis playback', 'libmad: mp1/2/3 playback', 'flac: flac playback', 'curl: lastfm scrobbler, shoutcast, icecast, podcast support', 'wavpack: wv playback', 'libsndfile: wav playback', "libcdio: audio cd plugin", "libcddb: audio cd plugin", "ffmpeg: for wma, aa3, oma, ac3, etc", "libmms: required for MMS protocol support", "faad2: required for AAC/MP4 support", "dbus: required for OSD notifications support", "pulseaudio: required for PulseAudio output plugin", "libx11: required for global hotkeys plugin", )
makedepends=('pkgconfig')
install=deadbeef.install
source=(http://downloads.sourceforge.net/project/$pkgname/$pkgname-$pkgver.tar.bz2)
md5sums=('204ce66fd864b2e2b6241532cc53a024')
options=('!libtool')

build() {
    cd $srcdir/$pkgname-$pkgver
    ./configure --prefix=/usr
    make || return 1
    make prefix=$pkgdir/usr install
}
