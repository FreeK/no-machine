# Maintainer: FreeK <stephan@confidr.me>
# Contributor: olav-st <olav.s.th@gmail.com>

pkgname=nomachine
pkgver=4.2.26
pkgrel=1
pkgdesc="Remote desktop application"
url="http://www.nomachine.com"
license=('custom:"Copyright 2002-2014 NoMachine S.à r.l."')
arch=('x86_64' 'i686')
options=('!strip')
conflicts=('nxmanager nxwebplayer nxserver nxnode nxclient')
install=nomachine.install

if [ "${CARCH}" = "x86_64" ]; then
  sha256sums=('eb0c82fa7ca966abe48b752c3643d844c93e762ea65ffc13caff75e2c5275778')
  _carch=_x86_64
elif [ "${CARCH}" = "i686" ]; then
  sha256sums=('163977f7ac32efe6430f9d11707546612a5914a9317ddd968b7cbbae43053500')
  _carch=_i686
fi
source=("http://download.nomachine.com/download/4.2/Linux/${pkgname}_${pkgver}_${pkgrel}${_carch}.tar.gz")

package()
{
  cd "${srcdir}"

  install -d "${pkgdir}/usr/"
  cp -a NX "${pkgdir}/usr/NX"
}
