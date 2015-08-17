# Author: Alexander Soudakov <cygakoB@gmail.com>
# Contributor: Charoite Lee <charoitehllee@live.com>
pkgname=perl-soap-transport-http-nginx
pkgver=0.01
pkgrel=2
pkgdesc='transport for nginx (<http://nginx.net/>) http server for SOAP::Lite module.'
arch=('any')
url='http://search.cpan.org/dist/SOAP-Transport-HTTP-Nginx'
license=('GPL' 'PerlArtistic')
depends=('perl-soap-lite')
makedepends=()
provides=('perl-soap-transport-http-nginx' 'perl-xmlrpc-transport-http-nginx')
conflicts=()
replaces=()
backup=()
options=('!emptydirs')
install=
source=("http://search.cpan.org/CPAN/authors/id/C/CY/CYGA/SOAP-Transport-HTTP-Nginx-$pkgver.tar.gz")
changelog=

build() {
  cd "$srcdir/SOAP-Transport-HTTP-Nginx-$pkgver"

  export PERL_MM_USE_DEFAULT=1 PERL_AUTOINSTALL=--skipdeps \
    PERL_MM_OPT="INSTALLDIRS=vendor DESTDIR='$pkgdir'" \
    PERL_MB_OPT="--installdirs vendor --destdir '$pkgdir'" \
    MODULEBUILDRC=/dev/null

  { /usr/bin/perl Makefile.PL &&
    make &&
    make test &&
    make install; } || return 1
}

md5sums=('807e3815fad5e13819015f265ba2f11c')
