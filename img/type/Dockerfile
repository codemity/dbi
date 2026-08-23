ARG VENDOR="vendor"

FROM ${VENDOR}/alpine:latest AS final

RUN apk add --no-cache bash nodejs npm \
    && npm install -g --omit=dev --no-update-notifier --no-fund quicktype@26.0.0 json-schema-to-typescript@15.0.4 \
    && npm cache clean --force \
    && rm -rf /root/.npm /root/.cache /tmp/* /var/tmp/*
