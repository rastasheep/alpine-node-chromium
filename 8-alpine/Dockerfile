FROM node:8-alpine

MAINTAINER Aleksandar Diklic "https://github.com/rastasheep"
# Credits: https://damianhodgkiss.com/articles/how-to-run-google-chrome-headless-and-nodejs-in-a-docker-container/
RUN \
  apk --no-cache  update \
  && apk --no-cache  upgrade \
  && echo "http://dl-2.alpinelinux.org/alpine/edge/main" > /etc/apk/repositories
  && echo "http://dl-2.alpinelinux.org/alpine/edge/community" >> /etc/apk/repositories
  && echo "http://dl-2.alpinelinux.org/alpine/edge/testing" >> /etc/apk/repositories
  && apk -U --no-cache \
      --allow-untrusted add \
      zlib-dev \
      chromium \
      xvfb \
      wait4ports \
      xorg-server \
      dbus \
      ttf-freefont \
      grep \
      udev \
      && apk del --purge --force linux-headers binutils-gold gnupg zlib-dev libc-utils \
      && rm -rf /var/lib/apt/lists/* \
      /var/cache/apk/* \
      /usr/share/man \
      /tmp/* \
      /usr/lib/node_modules/npm/man \
      /usr/lib/node_modules/npm/doc \
      /usr/lib/node_modules/npm/html \
      /usr/lib/node_modules/npm/scripts

ENV CHROME_BIN /usr/bin/chromium-browser
ENV LIGHTHOUSE_CHROMIUM_PATH /usr/bin/chromium-browser
