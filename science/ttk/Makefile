PORTNAME=	ttk
DISTVERSION=	1.1.0
PORTREVISION=	1
CATEGORIES=	science

MAINTAINER=	yuri@FreeBSD.org
COMMENT=	Topology ToolKit: Topological data analysis and visualization
WWW=		https://topology-tool-kit.github.io/

LICENSE=	BSD4CLAUSE
LICENSE_FILE=	${WRKSRC}/LICENSE

BROKEN_i386=	compilation fails: cannot initialize a parameter of type 'const ttk::LongSimplexId *' (aka 'const long long *') with an lvalue ..., see https://github.com/topology-tool-kit/ttk/issues/852

PY_DEPENDS=	${PYNUMPY} \
		${PYTHON_PKGNAMEPREFIX}scikit-build>0:devel/py-scikit-build@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}scipy>0:science/py-scipy@${PY_FLAVOR}
BUILD_DEPENDS=	${LOCALBASE}/include/boost/functional/hash.hpp:devel/boost-libs \
		cli11>0:devel/cli11 \
		exprtk>0:math/exprtk \
		spectra>0:math/spectra \
		utf8cpp>0:devel/utf8cpp \
		websocketpp>0:devel/websocketpp \
		${PY_DEPENDS}
BUILD_DEPENDS+=	nlohmann-json>0:devel/nlohmann-json # is required by lib/cmake/paraview-5.11/vtk/VTK-vtk-module-find-packages.cmake:1167
LIB_DEPENDS=	libcgraph.so:graphics/graphviz \
		libembree3.so:graphics/embree \
		libfreetype.so:print/freetype2 \
		libjsoncpp.so:devel/jsoncpp \
		libvtkRenderingCore-pv${PARAVIEW_VER}.so:science/paraview \
		libzfp.so:devel/zfp
RUN_DEPENDS=	${PY_DEPENDS}

USES=		cmake eigen:3 compiler:c++11-lang gl python sqlite xorg
USE_GL=		glew
USE_XORG=	x11

USE_GITHUB=	yes
GH_ACCOUNT=	topology-tool-kit

post-stage:
	${RM} ${STAGEDIR}${PREFIX}/include/Python.h

.include <../../science/paraview/Makefile.version>
.include <bsd.port.mk>
