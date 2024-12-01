# Maintainer: Tony Chou ngai.lam.chou@gmail.com

pkgname=recycler
pkgver=1.0
pkgrel=1
pkgdesc="A recycle bin for Arch Linux"
arch=('x86_64')
license=('GPL')
source=('recycler' 'LICENSE' 'recycler.service' 'recycler.timer')
md5sums=('SKIP' 'SKIP' 'SKIP' 'SKIP')

package() {
	install -Dm755 "/home/arch/file-landfill/src/recycler" "$pkgdir/usr/bin/recycler"
	install -Dm644 "/home/arch/file-landfill/src/LICENSE" "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
	sudo install -Dm644 "recycler.service" "$pkgdir/usr/lib/systemd/system/recycler.service"
	sudo install -Dm644 "recycler.timer" "$pkgddir/usr/lib/systemd/system/recycler.timer"
}	
