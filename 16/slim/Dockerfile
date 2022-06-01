#
#
#--------------------------------------------------------------------------
# node 16-slim
#--------------------------------------------------------------------------
#

ARG NODE_VERSION=16.15.0
FROM chinayin/node:${NODE_VERSION}
LABEL maintainer="chinayin <whereismoney@qq.com>"

ARG CHANGE_SOURCE=true
RUN if [ $CHANGE_SOURCE = true ]; then \
    npm config set registry https://registry.npmmirror.com -g && \
    yarn config set registry https://registry.npmmirror.com -g \
;fi && install_packages procps;

RUN set -eux; \
    \
    mkdir /app; \
    \
    node --version

USER node
WORKDIR /app
