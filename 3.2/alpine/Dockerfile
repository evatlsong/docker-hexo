FROM node:6.10-alpine

MAINTAINER evatlsong, <evatlsong@gmail.com>

WORKDIR /Hexo

RUN \
    npm install hexo-cli -g --registry=https://registry.npm.taobao.org\
    && hexo init . \
    && npm install --registry=https://registry.npm.taobao.org

VOLUME ["/Hexo/source", "/Hexo/themes"]

EXPOSE 80

COPY docker-entrypoint.sh /docker-entrypoint.sh

ENTRYPOINT ["/docker-entrypoint.sh"]

CMD ['/bin/bash']
