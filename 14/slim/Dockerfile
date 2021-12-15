#
#
#--------------------------------------------------------------------------
# node 14-slim
#--------------------------------------------------------------------------
#

FROM chinayin/node:14
LABEL maintainer="chinayin <whereismoney@qq.com>"

ENV NODE_VERSION 14.18.2

ARG CHANGE_SOURCE=true
RUN if [ $CHANGE_SOURCE = true ]; then \
    npm config set registry https://registry.npm.taobao.org -g && \
    yarn config set registry https://registry.npm.taobao.org -g \
;fi

RUN set -eux; \
    \
    mkdir /app; \
    \
    node --version

USER node
WORKDIR /app
