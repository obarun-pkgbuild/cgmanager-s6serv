# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=cgmanager-s6serv
pkgver=0.1
pkgrel=4
pkgdesc="cgmanager service for s6"
arch=(x86_64)
license=('beerware')
depends=('cgmanager' 's6' 's6-rc' 's6-boot')
conflicts=()
source=('cgmanager.daemon.run.s6'	
		'cgmanager.log.run.s6'
		'cgmanager.logd'
		'LICENSE')
md5sums=('73b9ac2d6c645dab647c3efe8c51ea57'
         '8dba8398d1fd78d9b8faf4d6aa2cb57d'
         '4b16a82b2693d98e6a3d29c56934dd60'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# daemon
	install -Dm 0755 "$srcdir/cgmanager.daemon.run.s6" "$pkgdir/etc/s6-serv/available/classic/cgmanager/run"
	
	# log
	install -Dm 0755 "$srcdir/cgmanager.log.run.s6" "$pkgdir/etc/s6-serv/available/classic/cgmanager/log/run"
	install -Dm 0644 "$srcdir/cgmanager.logd" "$pkgdir/etc/s6-serv/log.d/cgmanager"
	
	install -Dm 0755 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/cgmanager-s6serv/LICENSE"
}
