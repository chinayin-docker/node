#
#--------------------------------------------------------------------------
# Image Setup
#--------------------------------------------------------------------------
#

FROM chinayin/node:12
ENV DEPLOY_IMAGE_VERSION="2021-01-05 21:19"

RUN set -eux; \
    # Install pm2
    npm install pm2 -g; \
    \
    pm2 -version

EXPOSE 3000 43554

CMD ["pm2-runtime", "start", "pm2.json"]
