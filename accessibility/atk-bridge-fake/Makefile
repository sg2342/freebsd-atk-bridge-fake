# $FreeBSD$

PORTNAME=	atk-bridge-fake
PORTVERSION=	0.0.1
CATEGORIES=	accessibility	
MASTER_SITES=	# none
DISTFILES=	# none

MAINTAINER=	sg2342@googlemail.com
COMMENT=	dummy atk-bridge to be able to build gtk+3 without hard dbus deps

NO_BUILD=	yes
NO_WRKSUBDIR=	yes

SRC=		${.CURDIR}/src


CONFLICTS_INSTALL=	atk-spi2-atk

NO_BUILD=	yes

do-install:
	${MKDIR} ${STAGEDIR}${PREFIX}/include/at-spi2-atk/2.0
	${INSTALL_DATA} ${SRC}/atk-bridge.h ${STAGEDIR}${PREFIX}/include/
	${INSTALL_DATA} ${SRC}/atk-bridge-2.0.pc ${STAGEDIR}${PREFIX}/libdata/pkgconfig/
	${REINPLACE_CMD} -e 's|/usr/local|${PREFIX}|' \
		${STAGEDIR}${PREFIX}/libdata/pkgconfig/atk-bridge-2.0.pc


.include <bsd.port.mk>
