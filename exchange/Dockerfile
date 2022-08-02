FROM node:current

RUN apt-get update && apt-get install -y git unzip npm

WORKDIR /usr/src/app
RUN git clone https://github.com/Rey777/homepanda_exchange.git .
RUN npm install