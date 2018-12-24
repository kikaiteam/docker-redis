FROM redis:5.0.3-alpine

RUN apk add --no-cache bash

COPY docker-healthcheck /usr/local/bin/
HEALTHCHECK CMD ["docker-healthcheck"]

COPY docker-entrypoint /usr/local/bin/
ENTRYPOINT ["docker-entrypoint"]

CMD redis-server --appendonly yes --requirepass $REDIS_PASSWORD
