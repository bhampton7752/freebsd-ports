# $FreeBSD$

PORTNAME=	wlrobs
PORTVERSION=	s20200622
DISTVERSIONSUFFIX=	-1d3acaaf6404
CATEGORIES=	multimedia
#MASTER_SITES=	https://hg.sr.ht/~scoopta/${PORTNAME}/archive/${DISTVERSIONSUFFIX:S/^-//}${EXTRACT_SUFX}?dummy=/
MASTER_SITES+=	LOCAL/jbeich # https://todo.sr.ht/~sircmpwn/hg.sr.ht/33
DISTNAME=	${PORTNAME}${DISTVERSIONSUFFIX}

MAINTAINER=	jbeich@FreeBSD.org
COMMENT=	Wayland screen capture plugin for obs-studio

LICENSE=	GPLv3+
LICENSE_FILE=	${WRKSRC}/COPYING.md

LIB_DEPENDS=	libwayland-client.so:graphics/wayland \
		libobs.so:multimedia/obs-studio

USES=		compiler:c11 gl meson pkgconfig
USE_GL=		egl
DATADIR=	${PREFIX}/lib/obs-plugins
PORTDATA=	lib${PORTNAME}.so

# XXX Move to "pkg-config --cflags libobs"
CFLAGS_powerpc64=	-DNO_WARN_X86_INTRINSICS -maltivec -mvsx

.include <bsd.port.mk>
