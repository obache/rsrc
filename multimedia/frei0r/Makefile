# $NetBSD: Makefile,v 1.3 2020/08/17 20:17:37 leot Exp $

DISTNAME=	frei0r-plugins-1.7.0
PKGNAME=	${DISTNAME:S/-plugins//}
PKGREVISION=	1
CATEGORIES=	multimedia
MASTER_SITES=	https://files.dyne.org/frei0r/

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://frei0r.dyne.org/
COMMENT=	Collection of free and portable video plugins
LICENSE=	gnu-gpl-v2

USE_CMAKE=	yes
USE_TOOLS+=	pkg-config
USE_LANGUAGES=	c c++

CMAKE_ARGS+=	-DCMAKE_BUILD_TYPE="Release"
# Not in pkgsrc yet
CMAKE_ARGS+=	-DWITHOUT_GAVL=ON
# Not compatible with latest version
CMAKE_ARGS+=	-DWITHOUT_OPENCV=ON

.include "../../graphics/cairo/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
