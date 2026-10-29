# belzadur: das App-Abbild entsteht direkt aus dem hier gebauten Programm
# (.github/workflows/belzadur-addon.yml), nicht aus ghcr.io/wez/govee2mqtt:latest.
# Kontext ist die Wurzel des Repos.
ARG TARGETARCH
FROM ghcr.io/home-assistant/amd64-base-debian:bookworm AS base-amd64
FROM ghcr.io/home-assistant/aarch64-base-debian:bookworm AS base-arm64
FROM base-${TARGETARCH}
ARG TARGETPLATFORM
COPY addon/run.sh /run.sh
COPY docker-target/${TARGETPLATFORM}/govee /app/govee
COPY assets /app/assets/
COPY AmazonRootCA1.pem /app/
CMD [ "/run.sh" ]
