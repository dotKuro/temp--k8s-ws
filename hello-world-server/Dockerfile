FROM node:16

RUN mkdir /app
WORKDIR /app

ADD package.json .
ADD package-lock.json .
ADD main.js .
ADD public ./public/
RUN npm install

CMD node main.js
