PORTNAME=	google-cloud-pubsub
PORTVERSION=	2.15.2
CATEGORIES=	net rubygems
MASTER_SITES=	RG

MAINTAINER=	sunpoet@FreeBSD.org
COMMENT=	Official library for Google Cloud Pub/Sub
WWW=		https://github.com/googleapis/google-cloud-ruby/tree/main/google-cloud-pubsub

LICENSE=	APACHE20
LICENSE_FILE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	rubygem-concurrent-ruby>=1.1<2:devel/rubygem-concurrent-ruby \
		rubygem-google-cloud-core>=1.5<2:net/rubygem-google-cloud-core \
		rubygem-google-cloud-pubsub-v1>=0.8<1:net/rubygem-google-cloud-pubsub-v1 \
		rubygem-retriable>=3.1<4:devel/rubygem-retriable

USES=		gem

NO_ARCH=	yes

.include <bsd.port.mk>
