PORTNAME=	cq-editor
DISTVERSION=	0.1.2
PORTREVISION=	9
CATEGORIES=	cad
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	ports@nicandneal.net
COMMENT=	CadQuery GUI editor based on PyQT
WWW=		https://github.com/CadQuery/CQ-editor/

LICENSE=	APACHE20

DEPRECATED=	Depends on expiring cad/py-cadquery
EXPIRATION_DATE=2023-06-21

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}cadquery>=0:cad/py-cadquery@${PY_FLAVOR} \
		${PYTHON_SITELIBDIR}/spyder/__init__.py:devel/spyder

USES=		pyqt:5 python:3.6+
USE_PYTHON=	autoplist distutils
USE_PYQT=	pyqt5

USE_GITHUB=	yes
GH_ACCOUNT=	CadQuery
GH_PROJECT=	CQ-editor

.include <bsd.port.mk>
