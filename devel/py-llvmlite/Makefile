PORTNAME=	llvmlite
DISTVERSION=	0.41.0
CATEGORIES=	devel python
MASTER_SITES=	PYPI
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	dave@dal.ca
COMMENT=	Lightweight LLVM python binding for writing JIT compilers
WWW=		https://github.com/numba/llvmlite

LICENSE=	BSD3CLAUSE
LICENSE_FILE=	${WRKSRC}/LICENSE

BINARY_ALIAS=	c++=${LOCALBASE}/bin/clang++${LLVM_VERSION}
USES=		python fortran llvm:min=12,max=14,lib
USE_PYTHON=	distutils autoplist pytest
USE_GITHUB=	yes
USE_BINUTILS=	yes
GH_TUPLE=	numba:llvmlite:add17f8

CXXFLAGS+=	-fPIC

MAKE_ENV=	LLVM_CONFIG=${LLVM_CONFIG}

TEST_ENV=	${MAKE_ENV} PYTHONPATH=${STAGEDIR}${PYTHONPREFIX_SITELIBDIR}

post-install:
	@${STRIP_CMD} ${STAGEDIR}${PYTHON_SITELIBDIR}/llvmlite/binding/libllvmlite*.so

.include <bsd.port.mk>
