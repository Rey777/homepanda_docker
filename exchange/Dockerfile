FROM node:current

# install necessary packages
RUN apt-get update && apt-get install -y git unzip npm

# clone and initialize application
WORKDIR /usr/src/app
RUN git clone https://github.com/Rey777/homepanda_exchange.git .
RUN npm install