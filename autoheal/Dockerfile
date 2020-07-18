ARG arch=armv7
FROM multiarch/alpine:${arch}-v3.10

RUN apk add --no-cache curl jq
COPY docker-entrypoint /
ENTRYPOINT ["/docker-entrypoint"]

HEALTHCHECK --interval=5s CMD /docker-entrypoint healthcheck

CMD ["autoheal"]
