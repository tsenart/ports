# Created by: Jason Bacon <bacon4000@gmail.com>
# $FreeBSD$

PORTNAME=	qtermwidget
PORTVERSION=	0.7.0
CATEGORIES=	x11-toolkits

MAINTAINER=	bacon4000@gmail.com
COMMENT=	Terminal widget for QTerminal

LICENSE=	GPLv2

USES=		cmake:outsource compiler:c++11-lang pkgconfig tar:xz
USE_LDCONFIG=	yes
USE_QT5=	buildtools_build core gui qmake_build widgets

CMAKE_ARGS+=	-DBUILD_DESIGNER_PLUGIN:BOOL=OFF -DUSE_QT5:BOOL=ON

USE_GITHUB=	yes
GH_ACCOUNT=	lxde

.include <bsd.port.pre.mk>

.if ${OPSYS} == FreeBSD
CFLAGS+=	-DHAVE_UTEMPTER
.endif

.include <bsd.port.post.mk>
