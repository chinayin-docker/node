#
#
#--------------------------------------------------------------------------
# node 18-pm2
#--------------------------------------------------------------------------
#

ARG NODE_VERSION=18.15.0
FROM chinayin/node:${NODE_VERSION}-slim
LABEL maintainer="chinayin <whereismoney@qq.com>"

USER root
RUN set -eux; \
    # Install pm2
    npm install pm2 -g; \
    \
    pm2 -version

USER node
EXPOSE 3000 43554
CMD ["pm2-runtime", "start", "pm2.json"]
