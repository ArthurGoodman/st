pkgname=st-custom
_pkgname=st
pkgver=0.8.4
pkgrel=1
pkgdesc="A simple virtual terminal emulator for X."
arch=('any')
# url=""
license=('MIT')
depends=('libxft')
source=(
    FAQ
    LEGACY
    LICENSE
    Makefile
    README
    TODO
    arg.h
    config.def.h
    config.mk
    st.1
    st.c
    st.h
    st.info
    win.h
    x.c
    )

provides=('st')
conflicts=('st')

build() {
    cd "$srcdir"
    [ -f config.h ] && rm config.h
    make
}

package() {
    cd "$srcdir"
    make PREFIX=/usr DESTDIR="$pkgdir/" install
    install -m 0644 -D -t "$pkgdir/usr/share/licenses/$_pkgname" LICENSE
    install -m 0644 -D -t "$pkgdir/usr/share/doc/$_pkgname" README
    install -m 0644 -D -t "$pkgdir/usr/share/$_pkgname" st.info
}

md5sums=('SKIP'
         'SKIP'
         'SKIP'
         'SKIP'
         'SKIP'
         'SKIP'
         'SKIP'
         'SKIP'
         'SKIP'
         'SKIP'
         'SKIP'
         'SKIP'
         'SKIP'
         'SKIP'
         'SKIP')
