#
#
#--------------------------------------------------------------------------
# node 14-with-python
#--------------------------------------------------------------------------
#

ARG NODE_VERSION=14.21.3
FROM chinayin/node:${NODE_VERSION}-slim
LABEL maintainer="chinayin <whereismoney@qq.com>"

USER root
RUN set -eux; \
    # Install python
    install_packages python3 make g++; \
    ln -s /usr/bin/python3 /usr/bin/python; \
    \
    python -V

USER node
EXPOSE 3000 43554
CMD ["pm2-runtime", "start", "pm2.json"]
