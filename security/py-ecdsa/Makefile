PORTNAME=	ecdsa
PORTVERSION=	0.18.0
CATEGORIES=	security python
MASTER_SITES=	PYPI
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	sunpoet@FreeBSD.org
COMMENT=	ECDSA cryptographic signature library (pure python)
WWW=		https://github.com/tlsfuzzer/python-ecdsa

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}six>=1.9.0:devel/py-six@${PY_FLAVOR}
TEST_DEPENDS=	${PYTHON_PKGNAMEPREFIX}hypothesis>=0:devel/py-hypothesis@${PY_FLAVOR}

USES=		python:3.6+
USE_PYTHON=	autoplist concurrent distutils pytest

NO_ARCH=	yes

OPTIONS_RADIO=	FASTER
OPTIONS_RADIO_FASTER=	GMPY GMPY2
OPTIONS_DEFAULT=GMPY2
GMPY_DESC=	GMPY support
GMPY2_DESC=	GMPY2 support

GMPY_RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}gmpy>=0:math/py-gmpy@${PY_FLAVOR}
GMPY2_RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}gmpy2>=0:math/py-gmpy2@${PY_FLAVOR}

.include <bsd.port.mk>
