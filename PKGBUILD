# Maintainer: Andreas Mueller <amu@gnoppix.com>  

pkgname=gnoppix-zsh-config
pkgver=1.0.0
pkgrel=3
pkgdesc="Zsh configuration for Gnoppix"
arch=(any)
url="https://github.com/gnoppix/$pkgname"
license=(GPL-1.0-only)
depends=(
  fzf
  oh-my-zsh-git
  pkgfile
  powerline-fonts
  vim
  zsh
  zsh-autosuggestions
  zsh-completions
  zsh-history-substring-search
  zsh-syntax-highlighting
  zsh-theme-powerlevel10k
)
makedepends=(
  git
)
source=("git+$url.git#commit=2d809c457f78b935a4fb78719f7c7abac26b7caa")
md5sums=('764285832950473259b519024d76c924')

pkgver() {
    cd "$srcdir/$pkgname"
    printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
    cd $srcdir/$pkgname
    install -D -m644 gnoppix-config.zsh $pkgdir/usr/share/gnoppix-zsh-config/gnoppix-config.zsh
    install -D -m644 zshrc $pkgdir/etc/skel/.zshrc
}
