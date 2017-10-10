FROM node:8.6.0-alpine

MAINTAINER iyannik0215 , <admin@mashiro.io>


WORKDIR /Hexo
RUN sudo chown -R $USER:$(id -gn $USER) /root/.config
RUN \
    npm install hexo-cli -g \
    && hexo init . \
    && npm install \
    && npm install hexo-generator-sitemap --save \
    && npm install hexo-generator-feed --save \
    && npm install hexo-deployer-git --save

VOLUME ["/Hexo/source", "/Hexo/themes", "/root/.ssh"]

EXPOSE 80

COPY docker-entrypoint.sh /docker-entrypoint.sh

ENTRYPOINT ["/docker-entrypoint.sh"]

CMD ['/bin/bash']
