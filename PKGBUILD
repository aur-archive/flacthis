# Maintainer: precurse <andrewklaus AT gmail.com DOT com>

pkgname=flacthis
pkgver=1.1
pkgrel=2
pkgdesc="A multithreaded Python-based utility that converts lossless (FLAC,WAV) to lossy (MP3,AAC,FDK-AAC,OGG)" 
arch=('any')
url="http://code.google.com/p/flacthis/"
license=('BSD')
depends=('flac' 'lame' 'python2')
optdepends=(
  'ffmpeg-libfdk_aac: enhanced AAC encoder support'
  'faac: AAC encoder support'
  'mutagen: file ID3 tagging'
  'vorbis-tools: OGG audio encoding support'
)
source=(http://$pkgname.googlecode.com/git-history/v$pkgver/$pkgname.py
        http://$pkgname.googlecode.com/git-history/v$pkgver/audio_codecs.py)

sha256sums=('8fb7accf4c81c3f1e0401eb769faefa73a693a3dfbd84c556a6030d519b08f12'
           'e190804a6bf4a7e8c449a6a4bebbbbc663a48a9ea2d698622de68621ac574981')
package() {
	install -Dm755 $pkgname.py "$pkgdir"/usr/bin/$pkgname
        install -Dm755 audio_codecs.py "$pkgdir"/usr/bin/audio_codecs.py
}
