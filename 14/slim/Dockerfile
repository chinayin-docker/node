#
#
#--------------------------------------------------------------------------
# node 14-slim
#--------------------------------------------------------------------------
#

FROM chinayin/node:14
LABEL maintainer="chinayin <whereismoney@qq.com>"

ENV NODE_VERSION 14.17.1

ARG CHANGE_SOURCE=true
RUN if [ $CHANGE_SOURCE = true ]; then \
    npm config set registry https://registry.npm.taobao.org && \
    yarn config set registry https://registry.npm.taobao.org \
;fi

RUN set -eux; \
    \
    mkdir /app; \
    \
    node --version

USER node

WORKDIR /app
