#
#
#--------------------------------------------------------------------------
# node 16-pm2
#--------------------------------------------------------------------------
#

FROM chinayin/node:16-slim
LABEL maintainer="chinayin <whereismoney@qq.com>"

ENV NODE_VERSION 16.3.0

RUN set -eux; \
    # Install pm2
    npm install pm2 -g; \
    \
    pm2 -version

EXPOSE 3000 43554

CMD ["pm2-runtime", "start", "pm2.json"]
