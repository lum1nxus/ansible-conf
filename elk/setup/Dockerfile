# https://github.com/docker-library/repo-info/blob/master/repos/elasticsearch
# ElasticSearch:8.2.2
FROM elasticsearch@sha256:ba529600e5d761231f803feba56bb482bff047822c3e2097950db76ae67f7d60

USER root

COPY . /

RUN set -eux; \
	mkdir /state; \
	chown elasticsearch /state; \
	chmod +x /entrypoint.sh

USER elasticsearch:root

ENTRYPOINT ["/entrypoint.sh"]
