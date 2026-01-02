# Image with DNS+DNSSEC tools from BIND

FROM alpine:latest

# tzdata is required to use/set $TZ
RUN apk add --no-cache \
    bind-tools \
    bind-dnssec-tools \
    tzdata \
    && rm -rf /var/cache/apk/*

WORKDIR /data

# only echo list of tools as default command
CMD ["sh", "-c", "echo 'BIND Tools:' && echo '  DNS: named-checkzone, dig, nslookup, host' && echo '  DNSSEC: dnssec-keygen, dnssec-signzone, dnssec-dsfromkey, dnssec-verify' && echo '' && echo 'Usage: docker compose --profile tools run --rm tools <command>'"]
