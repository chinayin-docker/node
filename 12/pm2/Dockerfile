#
#--------------------------------------------------------------------------
# Image Setup
#--------------------------------------------------------------------------
#

FROM chinayin/node:12
ENV DEPLOY_IMAGE_VERSION="2021-01-05 16:04"

RUN set -eux; \
    # Install pm2
    npm install pm2 -g \
    \
    node --version

EXPOSE 3000 43554

CMD ["pm2-runtime", "start", "pm2.json"]
