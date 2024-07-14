# Maintainer: Sahil Gulihar sahilgullihar@gmail.com
pkgname=MediaSnip
pkgver=1.0.0
pkgrel=1
pkgdesc="A simple tool to download and trim videos and audios using yt-dlp and ffmpeg"
arch=('x86_64')
url="https://github.com/sahil-gulihar/mediasnip"
license=('MIT')
depends=('yt-dlp' 'ffmpeg' 'go')
source=("$pkgname-$pkgver.tar.gz::https://github.com/sahil-gulihar/mediasnip/archive/refs/tags/v$pkgver.tar.gz")
sha256sums=('09c480386d9423b58b8e03370a607892066fb94a9054f3e71906d41cfaeec50b')

build() {
    cd "$srcdir/$pkgname-$pkgver"
    go build -o mediasnipper .
}


package() {
    cd "$srcdir/$pkgname-$pkgver"
    install -Dm755 mediasnipper "$pkgdir/usr/bin/mediasnipper"
    install -Dm644 README.md "$pkgdir/usr/share/doc/$pkgname/README.md"
    install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

# vim:set ts=2 sw=2 et:

# https://github.com/Sahil-Gulihar/MediaSnip/archive/refs/tags/v1.0.0.tar.gz