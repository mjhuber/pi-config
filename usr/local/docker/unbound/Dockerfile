FROM alpine:3.8
EXPOSE 53
RUN apk update && \
    apk add unbound
COPY unbound.conf /etc/unbound/unbound.conf
CMD ["unbound", "-d"]
