# $NetBSD: Makefile,v 1.40 2021/04/21 11:41:20 adam Exp $

PKGNAME=	${PYPKGPREFIX}-sqlite3-${PY_DISTVERSION}
PKGREVISION=	19
CATEGORIES=	databases python

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://www.python.org/
COMMENT=	Built-in sqlite support for Python 2.5 and up

USE_GCC_RUNTIME=	yes

# part of python itself; using distutils.mk will install a useless egg
PYDISTUTILSPKG=		yes
PY_SETUP_SUBST+=	SQLITE_PREFIX=${BUILDLINK_PREFIX.sqlite3}

.include "../../databases/sqlite3/buildlink3.mk"
.include "../../lang/python/srcdist.mk"
.include "../../mk/bsd.pkg.mk"
