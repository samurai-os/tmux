# Maintainer: Paul Buzakov <paulbuzakov@gmail.com>
# Created for Samurai OS DevTeam based on Arch Linux
pkgname=samurai-os-tmux
pkgver=1.0.0
pkgrel=1
pkgdesc="A terminal multiplexer for the Samurai OS DevTeam."
arch=('x86_64' 'arm64')
url="https://github.com/samurai-os/tmux"
license=('Apache')
depends=('tmux' 'lazygit' 'mc')
source=('dotconfig/tmux')
sha256sums=('SKIP')

pkgver() {
    cd "$srcdir/dotconfig/tmux"
    git describe --tags --long --always | sed 's/^v//;s/-/./g'
}

package() {
    depends+=('tmux')

    install -d '$pkgdir/etc/samurai-os/tmux'
    cp -r "$srcdir/dotconfig/tmux" "$pkgdir/etc/samurai-os/tmux"

    depends+=('lazygit' 'mc')
}
