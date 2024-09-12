#
#
#--------------------------------------------------------------------------
# node 18-python
#--------------------------------------------------------------------------
#

ARG NODE_VERSION=18.20.4
FROM chinayin/node:${NODE_VERSION}-slim
LABEL maintainer="chinayin <whereismoney@qq.com>"

USER root
RUN set -eux; \
    # Install python
    install_packages python3 make g++; \
    ln -s /usr/bin/python3 /usr/bin/python; \
    \
    python -V
