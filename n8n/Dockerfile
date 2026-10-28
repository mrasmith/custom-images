FROM alpine:latest AS alpine

FROM docker.n8n.io/n8nio/n8n:latest

USER root

# Copy apk binary + required libs from Alpine
COPY --from=alpine /sbin/apk /sbin/apk
COPY --from=alpine /usr/lib/libapk.so* /usr/lib/

RUN apk add --no-cache \
    ffmpeg \
    imagemagick \
    tesseract-ocr \
    tesseract-ocr-data-eng

USER node
