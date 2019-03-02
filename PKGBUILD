# Maintainer: Facundo Tuesca <facutuesca AT gmail DOT com>

pkgname=streamtuner2
pkgver=2.2.1
pkgrel=1
pkgdesc="An internet radio browser"
arch=('any')
url="http://sourceforge.net/projects/streamtuner2"
license=('custom')
depends=('python2' 'pygtk' 'python2-xdg' 'python2-pillow' 'python2-keybinder2' 'python2-lxml' 'python2-cssselect' 'python2-pyquery' 'python2-requests')
makedepends=('libarchive')
source=("http://milki.include-once.org/streamtuner2/streamtuner2-2.2.1.bin.txz")
md5sums=('SKIP')

package() {
  # python2 fix
  sed -i 's:^#!.*/usr/bin/env.*python:#!/usr/bin/env python2:' "${srcdir}/usr/bin/${pkgname}"
  # Install launcher scripts
  install -m 755 -d "${pkgdir}/usr/bin"
  install -m 755 -d ${pkgdir}/usr/share/applications ${pkgdir}/usr/share/${pkgname}  ${pkgdir}/usr/share/pixmaps  ${pkgdir}/usr/share/man/man1  ${pkgdir}/usr/share/doc/streamtuner2
  
  install -m 755 usr/bin/${pkgname} ${pkgdir}/usr/bin/${pkgname}
  install -m 755 usr/share/applications/${pkgname}.desktop ${pkgdir}/usr/share/applications/
  cp -a usr/share/ ${pkgdir}/usr/
}
