# Maintainer: Paul Buzakov <paulbuzakov@gmail.com>
# Created for Samurai OS DevTeam based on Arch Linux
pkgname=samurai-os-tmux
pkgver=263656f
pkgrel=1
pkgdesc="A terminal multiplexer for the Samurai OS DevTeam."
arch=('x86_64' 'arm64')
url="https://github.com/samurai-os/tmux"
license=('Apache')
depends=('tmux' 'lazygit' 'mc')
source=('git+https://github.com/samurai-os/tmux.git')
sha256sums=('SKIP')
install=samurai-os-linux.install

pkgver() {
    cd "$srcdir/tmux/dotconfig/tmux"
    git describe --tags --long --always | sed 's/^v//;s/-/./g'
}

package() {
    install -d "$pkgdir/etc/samurai-os/tmux"
    cp -r "$srcdir/tmux/dotconfig/tmux" "$pkgdir/etc/samurai-os"
}
