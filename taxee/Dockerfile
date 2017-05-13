FROM node:alpine


RUN mkdir -p /home/app
WORKDIR /home/app
ADD . /home/app
# Install Bower & Gulp

RUN \
    npm cache clean \
    rm -Rf node_modules/ \
    npm install -g bower gulp \
    npm install \
    bower install --config.interactive=false --allow-root \

EXPOSE 9000

CMD gulp serve

