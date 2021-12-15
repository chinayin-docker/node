#
#
#--------------------------------------------------------------------------
# node 16-slim
#--------------------------------------------------------------------------
#

FROM chinayin/node:16
LABEL maintainer="chinayin <whereismoney@qq.com>"

ENV NODE_VERSION 16.13.1

ARG CHANGE_SOURCE=true
RUN if [ $CHANGE_SOURCE = true ]; then \
    npm config set registry https://registry.npm.taobao.org -g && \
    yarn config set registry https://registry.npm.taobao.org -g \
;fi && install_packages procps;

RUN set -eux; \
    \
    mkdir /app; \
    \
    node --version

USER node
WORKDIR /app
