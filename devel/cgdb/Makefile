# $OpenBSD: Makefile,v 1.10 2019/08/06 20:58:26 sthen Exp $

COMMENT=	curses GDB interface

DISTNAME=	cgdb-0.7.1

CATEGORIES=	devel

HOMEPAGE=	https://cgdb.github.io/

# GPLv2
PERMIT_PACKAGE=	Yes

WANTLIB=	${COMPILER_LIBCXX} c curses ereadline m util

COMPILER =		base-clang ports-gcc base-gcc

MASTER_SITES=	https://cgdb.me/files/

LIB_DEPENDS=	devel/readline>=6.1p2
RUN_DEPENDS=	devel/gdb

SEPARATE_BUILD=		Yes
CONFIGURE_STYLE=	autoconf
CONFIGURE_ARGS+=	--with-readline=yes
CONFIGURE_ENV=		LDFLAGS="-L${LOCALBASE}/lib" \
			CPPFLAGS="-I${LOCALBASE}/include/ereadline -I${LOCALBASE}/include"

AUTOCONF_VERSION=	2.69

# there are tests, but not working yet
NO_TEST=	Yes

.include <bsd.port.mk>
