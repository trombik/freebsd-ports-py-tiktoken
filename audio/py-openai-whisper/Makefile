PORTNAME=	openai-whisper
DISTVERSION=	20230314
CATEGORIES=	audio python
MASTER_SITES=	PYPI
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	y@trombik.org
COMMENT=	General-purpose speech recognition model by OpenAI

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	${BUILD_DEPENDS}
BUILD_DEPENDS=	${PYTHON_PKGNAMEPREFIX}tiktoken>0:audio/py-tiktoken@${PY_FLAVOR} \
	ffmpeg>0:multimedia/ffmpeg \
	${PYTHON_PKGNAMEPREFIX}numba>0:devel/py-numba@${PY_FLAVOR} \
	${PYTHON_PKGNAMEPREFIX}numpy>0:math/py-numpy@${PY_FLAVOR} \
	${PYTHON_PKGNAMEPREFIX}pytorch>0:misc/py-pytorch@${PY_FLAVOR} \
	${PYTHON_PKGNAMEPREFIX}tqdm>0:misc/py-tqdm@${PY_FLAVOR} \
	${PYTHON_PKGNAMEPREFIX}more-itertools>0:devel/py-more-itertools@${PY_FLAVOR} \
	${PYTHON_PKGNAMEPREFIX}ffmpeg-python>0:multimedia/py-ffmpeg-python@${PY_FLAVOR} \
	${PYTHON_PKGNAMEPREFIX}regex>0:textproc/py-regex@${PY_FLAVOR} \

WWW=	https://github.com/openai/whisper
USES=		python:3.9+
USE_PYTHON=	autoplist distutils
NO_ARCH=	yes

.include <bsd.port.mk>
