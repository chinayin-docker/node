#
#--------------------------------------------------------------------------
# Image Setup
#--------------------------------------------------------------------------
#

FROM node:14-buster-slim
LABEL maintainer="chinayin <whereismoney@qq.com>" Version="v14"
ENV DEBIAN_FRONTEND=noninteractive DEPLOY_IMAGE_VERSION="2021-01-05 15:48:31"

ARG CHANGE_SOURCE=true
ARG TIMEZONE=Asia/Shanghai
RUN if [ $CHANGE_SOURCE = true ]; then \
    sed -i 's/deb.debian.org/mirrors.aliyun.com/' /etc/apt/sources.list && \
    sed -i 's/security.debian.org/mirrors.aliyun.com/' /etc/apt/sources.list && \
    sed -i 's/security-cdn.debian.org/mirrors.aliyun.com/' /etc/apt/sources.list && \
    npm config set registry https://registry.npm.taobao.org && \
    yarn config set registry https://registry.npm.taobao.org
;fi && cp /usr/share/zoneinfo/$TIMEZONE /etc/localtime && echo "$TIMEZONE" > /etc/timezone;

RUN set -eux; \
    apt-get update; \
    apt-get autoremove -y; \
    apt-get upgrade -y; \
    apt-get install -y --no-install-recommends \
        apt-utils vim procps iputils-ping telnet \
    ; \
    apt-get clean; \
    rm -rf /var/lib/apt/lists/*; \
    printf "alias ls='ls --color=auto'\nalias ll='ls -l --color=auto'\nalias l='ls -lA --color=auto'" >> /root/.bashrc

RUN set -eux; \
    \
    mkdir /app; \
    \
    node --version

WORKDIR /app
