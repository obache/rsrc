# $NetBSD: Makefile,v 1.13 2020/01/18 23:35:19 rillig Exp $

DISTNAME=	mtscan-20050129
PKGREVISION=	1
CATEGORIES=	sysutils
MASTER_SITES=	# empty
DISTFILES=	# empty

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://mail-index.NetBSD.org/port-i386/2005/01/29/0011.html
COMMENT=	Magtape scanner - reports record and file-mark structure

NOT_FOR_PLATFORM=	Interix-*-* # no local tape ioctls

CPPFLAGS+=	-DMTIO

INSTALLATION_DIRS=	bin

do-extract:
	${CP} -R ${FILESDIR} ${WRKSRC}

do-build:
	cd ${WRKSRC} && ${CC} ${CFLAGS} ${CPPFLAGS} -o mtscan mtscan.c	\
		${LDFLAGS} ${BUILDLINK_LDADD.termcap}

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/mtscan ${DESTDIR}${PREFIX}/bin

.include "../../mk/termcap.buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
