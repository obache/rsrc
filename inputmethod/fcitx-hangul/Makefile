# $NetBSD$

DISTNAME=	fcitx-hangul-0.3.1
CATEGORIES=	inputmethod korean
MASTER_SITES=	http://download.fcitx-im.org/fcitx-hangul/
EXTRACT_SUFX=	.tar.xz

HOMEPAGE=	http://fcitx-im.org/
COMMENT=	Hangul Wrapper for Fcitx
LICENSE=	gnu-gpl-v2

USE_CMAKE=	yes
USE_LANGUAGES=	c c++
USE_TOOLS+=	msgfmt pkg-config

.include "../../inputmethod/fcitx/buildlink3.mk"
.include "../../inputmethod/libhangul/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
