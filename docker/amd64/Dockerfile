FROM mhart/alpine-node:11.2.0

WORKDIR /usr/src/app

RUN apk add --no-cache yarn

COPY server/package.json ./
COPY server/yarn.lock ./
COPY server/server.js ./

RUN yarn install

ADD frontend/dist ./

EXPOSE 49160
CMD ["yarn", "start"]
