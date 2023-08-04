PORTNAME=	tiktoken
DISTVERSION=	0.3.3
CATEGORIES=	audio python
MASTER_SITES=	PYPI
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	y@trombik.org
COMMENT=	Fast BPE tokeniser for use with OpenAI's models

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

BUILD_DEPENDS=	${PYTHON_PKGNAMEPREFIX}setuptools-rust>0:devel/py-setuptools-rust@${PY_FLAVOR}

WWW=	https://pypi.python.org/pypi/tiktoken
USES=		python:3.9+ cargo
USE_PYTHON=	autoplist distutils
BINARY_ALIAS=	python3=${PYTHON_CMD}
USE_GITHUB=	y
GH_TUPLE=	openai:tiktoken:${DISTVERSION}
CARGO_BUILD=	no
CARGO_INSTALL=	no
CARGO_CRATES=	aho-corasick-1.0.2 \
		autocfg-1.1.0 \
		bit-set-0.5.3 \
		bit-vec-0.6.3 \
		bitflags-1.3.2 \
		bstr-1.6.0 \
		cfg-if-1.0.0 \
		fancy-regex-0.10.0 \
		indoc-1.0.9 \
		libc-0.2.147 \
		lock_api-0.4.10 \
		memchr-2.5.0 \
		memoffset-0.6.5 \
		once_cell-1.18.0 \
		parking_lot-0.12.1 \
		parking_lot_core-0.9.8 \
		proc-macro2-1.0.66 \
		pyo3-0.17.3 \
		pyo3-build-config-0.17.3 \
		pyo3-ffi-0.17.3 \
		pyo3-macros-0.17.3 \
		pyo3-macros-backend-0.17.3 \
		quote-1.0.32 \
		redox_syscall-0.3.5 \
		regex-1.9.1 \
		regex-automata-0.3.4 \
		regex-syntax-0.7.4 \
		rustc-hash-1.1.0 \
		scopeguard-1.2.0 \
		serde-1.0.181 \
		smallvec-1.11.0 \
		syn-1.0.109 \
		target-lexicon-0.12.11 \
		unicode-ident-1.0.11 \
		unindent-0.1.11 \
		windows-targets-0.48.1 \
		windows_aarch64_gnullvm-0.48.0 \
		windows_aarch64_msvc-0.48.0 \
		windows_i686_gnu-0.48.0 \
		windows_i686_msvc-0.48.0 \
		windows_x86_64_gnu-0.48.0 \
		windows_x86_64_gnullvm-0.48.0 \
		windows_x86_64_msvc-0.48.0

.include <bsd.port.pre.mk>

post-build:
	${STRIP_CMD} ${WRKSRC}/target/release/lib_tiktoken.so*

.include <bsd.port.post.mk>
